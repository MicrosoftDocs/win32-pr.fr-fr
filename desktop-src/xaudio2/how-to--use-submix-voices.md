---
description: Cette rubrique vous montre comment définir des groupes de voix pour envoyer leur sortie à la même voix de mixage. Cela permet d’effectuer une seule modification sur une voix de mixage secondaire pour affecter un groupe entier de voix.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Procédure : utiliser des voix prémixées'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203628"
---
# <a name="how-to-use-submix-voices"></a><span data-ttu-id="606ec-104">Procédure : utiliser des voix prémixées</span><span class="sxs-lookup"><span data-stu-id="606ec-104">How to: Use Submix Voices</span></span>

<span data-ttu-id="606ec-105">Cette rubrique vous montre comment définir des groupes de voix pour envoyer leur sortie à la même voix de mixage.</span><span class="sxs-lookup"><span data-stu-id="606ec-105">This topic shows you how you can set groups of voices to send their output to the same submix voice.</span></span> <span data-ttu-id="606ec-106">Cela permet d’effectuer une seule modification sur une voix de mixage secondaire pour affecter un groupe entier de voix.</span><span class="sxs-lookup"><span data-stu-id="606ec-106">This enables a single change to a submix voice to affect a whole group of voices.</span></span>

1.  <span data-ttu-id="606ec-107">Créez une [**voix de mixage secondaire**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) à laquelle toutes les voix des effets sonores du jeu sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="606ec-107">Create a [**submix voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) to which all of the game's sound effect voices will send.</span></span>
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  <span data-ttu-id="606ec-108">Créer une [**XAUDIO2 \_ Voice \_ envoie**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) une structure qui contient une référence à la voix du mixage secondaire.</span><span class="sxs-lookup"><span data-stu-id="606ec-108">Create an [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure that contains a reference to the submix voice.</span></span>
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  <span data-ttu-id="606ec-109">Transmettez la [**XAUDIO2 \_ Voice \_ envoie**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) une structure aux nouvelles voix source au fur et à mesure de leur création.</span><span class="sxs-lookup"><span data-stu-id="606ec-109">Pass the [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure to new source voices as they are created.</span></span>
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  <span data-ttu-id="606ec-110">Appliquez les modifications à toutes les voix des effets sonores en réglant la voix du mixage secondaire.</span><span class="sxs-lookup"><span data-stu-id="606ec-110">Apply changes to all sound effect voices by adjusting the submix voice.</span></span>

    <span data-ttu-id="606ec-111">Dans cet exemple, la modification du volume de la voix de mixage secondaire avec la fonction [**setVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) modifie efficacement le volume de toutes les voix qui lui sont produites.</span><span class="sxs-lookup"><span data-stu-id="606ec-111">In this example, changing the volume of the submix voice with the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function effectively changes the volume of all voices that output to it.</span></span>

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="606ec-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="606ec-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="606ec-113">Voix</span><span class="sxs-lookup"><span data-stu-id="606ec-113">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="606ec-114">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="606ec-114">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="606ec-115">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="606ec-115">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
