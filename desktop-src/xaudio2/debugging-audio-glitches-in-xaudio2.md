---
description: Des problèmes peuvent se produire dans XAudio2, cette rubrique décrit comment ils sont signalés et certaines approches pour les résoudre.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Débogage des problèmes audio dans XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866494"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a><span data-ttu-id="fe8c5-103">Débogage des problèmes audio dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="fe8c5-103">Debugging Audio Glitches in XAudio2</span></span>

<span data-ttu-id="fe8c5-104">Des problèmes peuvent se produire dans XAudio2, cette rubrique décrit comment ils sont signalés et certaines approches pour les résoudre.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-104">Glitches can occur in XAudio2, this topic covers how they are reported and some approaches to fixing them.</span></span>

<span data-ttu-id="fe8c5-105">Cette présentation couvre les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe8c5-105">This overview covers the following topics:</span></span>

-   [<span data-ttu-id="fe8c5-106">Causes de problèmes ou de problèmes de sortie audio</span><span class="sxs-lookup"><span data-stu-id="fe8c5-106">Causes of audio output problems or glitches</span></span>](#causes-of-audio-output-problems-or-glitches)
-   [<span data-ttu-id="fe8c5-107">Comment XAudio2 signale les problèmes</span><span class="sxs-lookup"><span data-stu-id="fe8c5-107">How XAudio2 reports problems</span></span>](#how-xaudio2-reports-problems)
-   [<span data-ttu-id="fe8c5-108">Approches de la résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="fe8c5-108">Approaches to fixing problems</span></span>](#approaches-to-fixing-problems)
-   [<span data-ttu-id="fe8c5-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe8c5-109">Related topics</span></span>](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a><span data-ttu-id="fe8c5-110">Causes de problèmes ou de problèmes de sortie audio</span><span class="sxs-lookup"><span data-stu-id="fe8c5-110">Causes of audio output problems or glitches</span></span>

<span data-ttu-id="fe8c5-111">Des problèmes peuvent se produire dans la sortie XAudio2 pour plusieurs raisons.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-111">Glitches can occur in XAudio2 output for several reasons.</span></span>

-   <span data-ttu-id="fe8c5-112">Une voix source XAudio2 est en privé.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-112">An XAudio2 source voice is starved.</span></span> <span data-ttu-id="fe8c5-113">Le client n’envoie pas de son actualisé suffisamment rapidement.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-113">The client is not submitting fresh audio to it fast enough.</span></span> <span data-ttu-id="fe8c5-114">Vous recevez un silence, car il n’a pas de données à lire.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-114">You get silence because it has no data to play.</span></span>
-   <span data-ttu-id="fe8c5-115">XAudio2 dans son ensemble est surchargé.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-115">XAudio2 as a whole is overburdened.</span></span> <span data-ttu-id="fe8c5-116">Elle prend plus de *x* ms pour produire *X* ms de l’audio.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-116">It takes longer than *X* ms to produce *X* ms of audio.</span></span> <span data-ttu-id="fe8c5-117">Vous obtenez des pertes, car XAudio2 ne peut pas produire de données aussi rapidement que le périphérique audio en a besoin.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-117">You get dropouts because XAudio2 can't produce data as fast as the audio device needs it.</span></span> <span data-ttu-id="fe8c5-118">Il se peut que vous exécutiez trop de voix ou d’effets à la fois, en effectuant trop de tâches dans les rappels XAudio2 ou en effectuant des appels d’API XAudio2 trop fréquents.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-118">You might be running too many voices or effects at a time, doing too much work in XAudio2 callbacks, or making XAudio2 API calls too frequently.</span></span>
-   <span data-ttu-id="fe8c5-119">Le thread de traitement audio s’arrête car l’implémentation du client d’un rappel XAudio2 fait des choses qui peuvent bloquer le thread.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-119">The audio processing thread is stalling because the client's implementation of some XAudio2 callback is doing things that can block the thread.</span></span> <span data-ttu-id="fe8c5-120">Par exemple, il peut accéder au disque, se synchroniser avec d’autres threads ou appeler d’autres fonctions qui peuvent se bloquer.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-120">For example, it might be accessing the disk, synchronizing with other threads, or calling other functions that may block.</span></span> <span data-ttu-id="fe8c5-121">Utilisez un thread d’arrière-plan de priorité inférieure que le rappel peut signaler pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-121">Use a lower-priority background thread that the callback can signal to perform such tasks.</span></span>
-   <span data-ttu-id="fe8c5-122">Le système dans son ensemble est surchargé.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-122">The system as a whole is overloaded.</span></span> <span data-ttu-id="fe8c5-123">Les autres threads qui s’exécutent avec une priorité identique ou supérieure à XAudio2 font trop de travail.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-123">Other threads running at the same or higher priority than XAudio2 are doing too much work.</span></span> <span data-ttu-id="fe8c5-124">Ils sont en concurrence avec le thread audio pour le temps processeur.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-124">They are competing with the audio thread for CPU time.</span></span>

## <a name="how-xaudio2-reports-problems"></a><span data-ttu-id="fe8c5-125">Comment XAudio2 signale les problèmes</span><span class="sxs-lookup"><span data-stu-id="fe8c5-125">How XAudio2 reports problems</span></span>

<span data-ttu-id="fe8c5-126">XAudio2 peut communiquer des problèmes dans la version de débogage de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-126">XAudio2 can communicate glitches in the debug build in several ways.</span></span>

-   <span data-ttu-id="fe8c5-127">Si une voix est déplacée, XAudio2 affiche un message dans ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-127">If a voice is being starved, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   <span data-ttu-id="fe8c5-128">Si le thread audio s’exécute trop longtemps, XAudio2 affiche un message dans ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-128">If the audio thread runs for too long, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    <span data-ttu-id="fe8c5-129">En règle générale, ce message s’affiche avec le message suivant.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-129">Typically, this message occurs with the next message.</span></span>

-   <span data-ttu-id="fe8c5-130">Si le pilote audio ne peut pas alimenter de nouvelles données audio à temps, XAudio2 affiche un message dans ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-130">If the audio driver can't be fed new audio data on time, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   <span data-ttu-id="fe8c5-131">L’appel de [**IXAudio2 :: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fournit des données de performance XAudio2, notamment le nombre total de problèmes depuis le démarrage du moteur XAudio2.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-131">Calling [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) provides XAudio2 performance data, including the total number of glitches since the XAudio2 engine started.</span></span>

## <a name="approaches-to-fixing-problems"></a><span data-ttu-id="fe8c5-132">Approches de la résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="fe8c5-132">Approaches to fixing problems</span></span>

<span data-ttu-id="fe8c5-133">Les méthodes possibles pour réduire les problèmes audio sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe8c5-133">Possible ways to reduce audio glitches include the following.</span></span>

-   <span data-ttu-id="fe8c5-134">Dans le cas de la privation de voix : augmentez la quantité de données audio mises en file d’attente sur une voix.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-134">In the voice starvation case: Increase the amount of audio data that is queued ahead on a voice.</span></span> <span data-ttu-id="fe8c5-135">Vous pouvez utiliser [**IXAudio2SourceVoice :: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) pour découvrir le nombre de mémoires tampons mises en file d’attente à tout moment.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-135">You can use [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) to discover the number of buffers queued at any moment.</span></span> <span data-ttu-id="fe8c5-136">Si vous voyez toujours des erreurs de privation de voix, mais que vous ne pouvez pas entendre de problème, assurez-vous que vous définissez la [**\_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Signale** à \_ \_ la fin du \_ flux XAUDIO2 sur la mémoire tampon finale d’un son.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-136">If you still see voice starvation errors, but can't hear any glitch, make sure you are setting [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flags** to XAUDIO2\_END\_OF\_STREAM on the final buffer of a sound.</span></span> <span data-ttu-id="fe8c5-137">Cela indique à XAudio2 de ne pas s’attendre à ce qu’un plus grand nombre de mémoires tampons soient nécessairement disponibles dès que celui-ci se termine.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-137">This tells XAudio2 not to expect any more buffers necessarily to be available as soon as this one completes.</span></span>

    <span data-ttu-id="fe8c5-138">Dans les autres cas :</span><span class="sxs-lookup"><span data-stu-id="fe8c5-138">In the other cases:</span></span>

    -   <span data-ttu-id="fe8c5-139">Réduisez le nombre de voix et d’effets actifs dans le graphique, en particulier les effets coûteux tels que la réverbération.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-139">Reduce the number of active voices and effects in the graph, especially expensive effects like reverb.</span></span>
    -   <span data-ttu-id="fe8c5-140">Désactivez les voix et les effets que vous n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-140">Disable voices and effects you're not using.</span></span>
    -   <span data-ttu-id="fe8c5-141">Utilisez les \_ indicateurs XAUDIO2 Voice \_ NOSRC et XAUDIO2 \_ voix \_ notonale dans [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-141">Use the XAUDIO2\_VOICE\_NOSRC and XAUDIO2\_VOICE\_NOPITCH flags in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), whenever possible.</span></span> <span data-ttu-id="fe8c5-142">La conversion du taux d’échantillonnage est coûteuse.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-142">Sample rate conversion is costly.</span></span>
    -   <span data-ttu-id="fe8c5-143">Réduisez le taux d’échantillonnage des voix individuelles.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-143">Reduce the sample rate of individual voices.</span></span> <span data-ttu-id="fe8c5-144">Par exemple, une voix de mixage secondaire hébergeant un effet de réverbération peut avoir un taux d’échantillonnage inférieur à celui de la voix source qui l’envoie.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-144">For example, a submix voice hosting a reverb effect can have a lower sample rate than the source voice sending to it.</span></span> <span data-ttu-id="fe8c5-145">Des sons tels que des explosions et des gunshots qui n’ont pas besoin d’une haute fidélité peuvent également être enregistrés à des taux d’échantillonnage inférieurs.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-145">Sounds such as explosions and gunshots that don't need high fidelity can also be recorded at lower sample rates.</span></span>
    -   <span data-ttu-id="fe8c5-146">Assurez-vous que les implémentations de rappel fonctionnent aussi peu que possible et ne sont jamais bloquées.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-146">Ensure that callback implementations do as little work as possible and never block.</span></span>
    -   <span data-ttu-id="fe8c5-147">Effectuez moins d’appels à XAudio2.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-147">Make fewer calls to XAudio2.</span></span> <span data-ttu-id="fe8c5-148">En règle générale, les paramètres audio n’ont pas besoin d’être mis à jour pour chaque image vidéo.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-148">Audio parameters usually don't need to be updated for every video frame.</span></span> <span data-ttu-id="fe8c5-149">Toutes les 30 ms suffisent.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-149">Every 30 ms or so is sufficient.</span></span> <span data-ttu-id="fe8c5-150">Vous devez éliminer les appels redondants, tels que le réglage du volume plusieurs fois en succession rapide.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-150">You should eliminate redundant calls, such as setting volume several times in quick succession.</span></span>
    -   <span data-ttu-id="fe8c5-151">Réduisez l’utilisation globale du processeur par le jeu.</span><span class="sxs-lookup"><span data-stu-id="fe8c5-151">Reduce the game's overall CPU usage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe8c5-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe8c5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe8c5-153">Fonctions de débogage</span><span class="sxs-lookup"><span data-stu-id="fe8c5-153">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="fe8c5-154">Référence de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="fe8c5-154">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
