---
description: Vous pouvez modifier les graphiques audio à tout moment pour ajouter ou supprimer des voix ou des sous-graphiques entiers.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Procédure : Ajouter ou supprimer dynamiquement des voix d’un graphique audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113651"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a><span data-ttu-id="f7b79-103">Procédure : Ajouter ou supprimer dynamiquement des voix d’un graphique audio</span><span class="sxs-lookup"><span data-stu-id="f7b79-103">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>

<span data-ttu-id="f7b79-104">Vous pouvez modifier les graphiques audio à tout moment pour ajouter ou supprimer des voix ou des sous-graphiques entiers.</span><span class="sxs-lookup"><span data-stu-id="f7b79-104">You can change audio graphs at any time to add or remove voices or entire subgraphs.</span></span> <span data-ttu-id="f7b79-105">Cette rubrique vous montre comment ajouter ou supprimer des voix de mixage secondaire d’un graphique qui a été créé en suivant les étapes décrites dans [Comment : générer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="f7b79-105">This topic shows you how to add or remove submix voices from a graph that has been created following the steps in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="f7b79-106">Une seule voix peut envoyer sa sortie à plusieurs voix ou à une longue chaîne de voix.</span><span class="sxs-lookup"><span data-stu-id="f7b79-106">A single voice can send its output to several voices or to a long chain of voices.</span></span> <span data-ttu-id="f7b79-107">La suppression ou l’ajout d’une seule voix peut avoir un impact important sur un graphique audio.</span><span class="sxs-lookup"><span data-stu-id="f7b79-107">Removing or adding a single voice can have a large effect on an audio graph.</span></span>

## <a name="to-dynamically-change-an-audio-graph"></a><span data-ttu-id="f7b79-108">Pour modifier dynamiquement un graphique audio</span><span class="sxs-lookup"><span data-stu-id="f7b79-108">To dynamically change an audio graph</span></span>

<span data-ttu-id="f7b79-109">L’ajout et la suppression de voix d’un graphique audio sont très similaires à l’ajout ou à la suppression de nœuds d’une liste ou d’un graphique à liaison unique.</span><span class="sxs-lookup"><span data-stu-id="f7b79-109">Adding and removing voices from an audio graph is very similar to adding or removing nodes from a single-linked list or graph.</span></span>

-   <span data-ttu-id="f7b79-110">Pour ajouter une voix ou un sous-graphe à un graphique audio</span><span class="sxs-lookup"><span data-stu-id="f7b79-110">To add a voice or subgraph to an audio graph</span></span>

    <span data-ttu-id="f7b79-111">Définissez la sortie d’une voix dans le graphique, la voix parente, sur la voix à ajouter à l’aide de la fonction [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) .</span><span class="sxs-lookup"><span data-stu-id="f7b79-111">Set the output of a voice in the graph, the parent voice, to the voice to be added using the [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) function.</span></span> <span data-ttu-id="f7b79-112">Définissez la sortie de la nouvelle voix sur l’enfant d’origine de la voix parente.</span><span class="sxs-lookup"><span data-stu-id="f7b79-112">Set the output of the new voice to the original child of the parent voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   <span data-ttu-id="f7b79-113">Pour supprimer une voix ou un sous-graphique d’un graphique audio</span><span class="sxs-lookup"><span data-stu-id="f7b79-113">To remove a voice or subgraph from an audio graph</span></span>

    <span data-ttu-id="f7b79-114">Définissez la voix de sortie du parent de la voix en cours de suppression sur l’enfant de la voix en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="f7b79-114">Set the output voice of the parent of the voice being removed to the child of the voice being removed.</span></span> <span data-ttu-id="f7b79-115">Si la voix en cours de suppression se trouve à la fin du graphique, la voix parente doit être modifiée pour pointer vers la voix principale.</span><span class="sxs-lookup"><span data-stu-id="f7b79-115">If the voice being removed is at the end of the graph, the parent voice should be changed to point to the master voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

<span data-ttu-id="f7b79-116">Notez que, par souci de clarté, chaque parent n’a qu’un seul enfant dans ces exemples.</span><span class="sxs-lookup"><span data-stu-id="f7b79-116">Note that for clarity each parent only has one child in these examples.</span></span> <span data-ttu-id="f7b79-117">Si un nœud parent a plusieurs enfants, son sendlist contient un tableau de voix au lieu d’un pointeur vers une seule voix.</span><span class="sxs-lookup"><span data-stu-id="f7b79-117">If a parent node has multiple children, its sendlist will contain an array of voices instead of a pointer to just one voice.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7b79-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7b79-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7b79-119">Graphiques audio</span><span class="sxs-lookup"><span data-stu-id="f7b79-119">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="f7b79-120">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="f7b79-120">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="f7b79-121">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="f7b79-121">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="f7b79-122">Procédure : utiliser des voix prémixées</span><span class="sxs-lookup"><span data-stu-id="f7b79-122">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="f7b79-123">Procédure : Créer une chaîne d’effets</span><span class="sxs-lookup"><span data-stu-id="f7b79-123">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
