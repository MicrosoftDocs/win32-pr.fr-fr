---
description: L’ensemble de toutes les voix, avec leurs effets contenus et leurs interconnexions, est appelé graphique de traitement audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Graphique audio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210804"
---
# <a name="xaudio2-audio-graph"></a><span data-ttu-id="6f1e0-103">Graphique audio XAudio2</span><span class="sxs-lookup"><span data-stu-id="6f1e0-103">XAudio2 Audio Graph</span></span>

<span data-ttu-id="6f1e0-104">L’ensemble de toutes les voix, avec leurs effets contenus et leurs interconnexions, est appelé graphique de traitement audio.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-104">The set of all voices, with their contained effects and their interconnections, is referred to as the audio processing graph.</span></span> <span data-ttu-id="6f1e0-105">Le graphique prend un ensemble de flux audio du client comme entrée, les traite et remet le résultat final à un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-105">The graph takes a set of audio streams from the client as input, processes them, and delivers the final result to an audio device.</span></span> <span data-ttu-id="6f1e0-106">Tout le traitement audio a lieu dans un thread distinct avec une périodicité définie par le quantum du graphique (actuellement 10 millisecondes sur Microsoft Windows et 5 1/3 millisecondes sur Xbox 360).</span><span class="sxs-lookup"><span data-stu-id="6f1e0-106">All audio processing takes place in a separate thread with a periodicity defined by the graph's quantum (currently 10 milliseconds on Microsoft Windows, and 5 1/3 milliseconds on Xbox 360).</span></span> <span data-ttu-id="6f1e0-107">Chaque Quantum en millisecondes, le thread sort et réitère les millisecondes de quantum des données audio dans le graphique entier.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-107">Every quantum milliseconds, the thread wakes up and disperses quantum milliseconds of audio data through the entire graph.</span></span> <span data-ttu-id="6f1e0-108">Pour obtenir un exemple de création d’un graphique audio de base, consultez Comment : [générer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="6f1e0-108">For an example of building a basic audio graph, see How to: [Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span>

<span data-ttu-id="6f1e0-109">Graphique audio simple :</span><span class="sxs-lookup"><span data-stu-id="6f1e0-109">A simple audio graph:</span></span>

![graphique audio simple](images/xaudio2-audio-graph.png)

<span data-ttu-id="6f1e0-111">Le client peut contrôler l’état du graphique de façon dynamique lorsqu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-111">The client can control the graph's state dynamically while it is running.</span></span> <span data-ttu-id="6f1e0-112">Les actions de contrôle peuvent inclure l’ajout et la suppression d’entrées et de sorties, la modification des effets internes et des interconnexions, la définition de paramètres sur les effets, l’activation et la désactivation des parties du graphique, etc.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-112">Control actions might include adding and removing inputs and outputs, changing the internal effects and interconnections, setting parameters on the effects, enabling and disabling parts of the graph, and so on.</span></span> <span data-ttu-id="6f1e0-113">Pour obtenir un exemple de modification dynamique d’un graphique audio, consultez [Comment : ajouter dynamiquement ou supprimer des voix d’un graphique audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="6f1e0-113">For an example of dynamically changing an audio graph, see [How to: Dynamically Add or Remove Voices From an Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span></span>

## <a name="processing-the-graph"></a><span data-ttu-id="6f1e0-114">Traitement du graphique</span><span class="sxs-lookup"><span data-stu-id="6f1e0-114">Processing the Graph</span></span>

<span data-ttu-id="6f1e0-115">Tout appel de méthode qui affecte un objet dans le graphique est considéré comme un changement d’état de graphique.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-115">Any method call that affects any object in the graph is considered to be effecting a graph state change.</span></span> <span data-ttu-id="6f1e0-116">Les modifications de l’état du graphique sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f1e0-116">Graph state changes include the following:</span></span>

-   <span data-ttu-id="6f1e0-117">Création et destruction de voix</span><span class="sxs-lookup"><span data-stu-id="6f1e0-117">Creating and destroying voices</span></span>
-   <span data-ttu-id="6f1e0-118">Démarrage ou arrêt des voix</span><span class="sxs-lookup"><span data-stu-id="6f1e0-118">Starting or stopping voices</span></span>
-   <span data-ttu-id="6f1e0-119">Modification des destinations d’une voix</span><span class="sxs-lookup"><span data-stu-id="6f1e0-119">Changing the destinations of a voice</span></span>
-   <span data-ttu-id="6f1e0-120">Modification des chaînes d’effets</span><span class="sxs-lookup"><span data-stu-id="6f1e0-120">Modifying effect chains</span></span>
-   <span data-ttu-id="6f1e0-121">Activation ou désactivation des effets</span><span class="sxs-lookup"><span data-stu-id="6f1e0-121">Enabling or disabling effects</span></span>
-   <span data-ttu-id="6f1e0-122">Définition des paramètres sur les effets ou sur les SRCs, filtres, volumes et mixages intégrés</span><span class="sxs-lookup"><span data-stu-id="6f1e0-122">Setting parameters on the effects or on the built-in SRCs, filters, volumes, and mixers</span></span>

<span data-ttu-id="6f1e0-123">Tout ensemble de modifications d’état de graphique peut être combiné et exécuté comme une transaction atomique.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-123">Any set of graph state changes can be combined and performed as an atomic transaction.</span></span> <span data-ttu-id="6f1e0-124">Ces opérations atomiques sont appelées ensembles d’opérations.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-124">These atomic operations are known as operation sets.</span></span> <span data-ttu-id="6f1e0-125">Elles sont abordées dans la vue d’ensemble des [ensembles d’opérations XAudio2](xaudio2-operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1e0-125">They are discussed in the [XAudio2 Operation Sets](xaudio2-operation-sets.md) overview.</span></span>

## <a name="internal-data-representation"></a><span data-ttu-id="6f1e0-126">Représentation des données internes</span><span class="sxs-lookup"><span data-stu-id="6f1e0-126">Internal Data Representation</span></span>

<span data-ttu-id="6f1e0-127">Les données audio dans le graphique XAudio2 sont toujours stockées et traitées dans un formulaire PCM à virgule flottante 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-127">Audio data within the XAudio2 graph is always stored and processed in 32-bit floating-point PCM form.</span></span> <span data-ttu-id="6f1e0-128">Toutefois, le nombre de canaux et le taux d’échantillonnage peuvent varier dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-128">However, the channel count and sample rate can vary within the graph.</span></span> <span data-ttu-id="6f1e0-129">Le format dans lequel une voix donnée traite les données audio est déterminé par le type de voix et les paramètres utilisés pour créer la voix.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-129">The format in which a given voice processes audio is determined by the voice type and parameters used to create the voice.</span></span>



| <span data-ttu-id="6f1e0-130">Type de voix</span><span class="sxs-lookup"><span data-stu-id="6f1e0-130">Voice Type</span></span>                                                                                                      | <span data-ttu-id="6f1e0-131">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f1e0-131">Parameters</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f1e0-132">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="6f1e0-132">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | <span data-ttu-id="6f1e0-133">Nombre de canaux et taux d’échantillonnage des voix auxquelles la voix source envoie de l’audio.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-133">The channel count and sample rate of the voices to which the source voice sends audio.</span></span>         |
| <span data-ttu-id="6f1e0-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) et [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span><span class="sxs-lookup"><span data-stu-id="6f1e0-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) and [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span></span> | <span data-ttu-id="6f1e0-135">Arguments *InputChannels* et *InputSampleRate* utilisés pour créer la voix de mixage secondaire/de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-135">The *InputChannels* and *InputSampleRate* arguments used to create the submix/mastering voice.</span></span> |



 

## <a name="format-conversion"></a><span data-ttu-id="6f1e0-136">Conversion de format</span><span class="sxs-lookup"><span data-stu-id="6f1e0-136">Format Conversion</span></span>

<span data-ttu-id="6f1e0-137">XAudio2 gère les taux d’échantillonnage ou les conversions de canaux qui sont nécessaires à l’audio transit d’une voix à l’autre, avec les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6f1e0-137">XAudio2 handles any sample rate or channel conversions that are required as audio travels from one voice to another, with the following limitations:</span></span>

-   <span data-ttu-id="6f1e0-138">Toutes les voix de destination pour une voix particulière doivent s’exécuter au même taux d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="6f1e0-138">All destination voices for a particular voice must be running at the same sample rate</span></span>
-   <span data-ttu-id="6f1e0-139">Les effets dans une chaîne d’effet peuvent modifier le nombre de canaux audio, mais pas son taux d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="6f1e0-139">Effects in an effect chain can change the audio's channel count, but not its sample rate</span></span>
-   <span data-ttu-id="6f1e0-140">Le nombre de canaux de sortie d’une chaîne d’effets doit correspondre à celui des voix qu’il envoie</span><span class="sxs-lookup"><span data-stu-id="6f1e0-140">An effect chain's output channel count must match that of the voices to which it sends</span></span>
-   <span data-ttu-id="6f1e0-141">Aucune modification de graphique dynamique ne peut être effectuée, ce qui rompt les règles ci-dessus</span><span class="sxs-lookup"><span data-stu-id="6f1e0-141">No dynamic graph change can be made which would break the rules above</span></span>

<span data-ttu-id="6f1e0-142">Du côté de l’entrée, les voix source peuvent lire les données dans n’importe quel format PCM valide, ou dans n’importe quel format compressé pris en charge par XAudio2.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-142">On the input side, source voices can read data in any valid PCM format, or in any of the compressed formats supported by XAudio2.</span></span> <span data-ttu-id="6f1e0-143">Si les données d’entrée sont compressées, elles sont décodées en PCM à virgule flottante avant tout traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-143">If the input data is compressed, it is decoded to floating-point PCM before any further processing is done.</span></span>

<span data-ttu-id="6f1e0-144">Du côté de la sortie, la maîtrise des voix peut uniquement produire des données PCM.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-144">On the output side, mastering voices can only produce PCM data.</span></span> <span data-ttu-id="6f1e0-145">Ces données satisferont toujours les mêmes restrictions que celles décrites ci-dessus pour les données PCM d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6f1e0-145">This data will always satisfy the same restrictions described above for input PCM data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f1e0-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f1e0-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f1e0-147">Graphiques audio</span><span class="sxs-lookup"><span data-stu-id="6f1e0-147">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="6f1e0-148">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="6f1e0-148">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6f1e0-149">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="6f1e0-149">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="6f1e0-150">Procédure : Ajouter ou supprimer dynamiquement des voix d’un graphique audio</span><span class="sxs-lookup"><span data-stu-id="6f1e0-150">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[<span data-ttu-id="6f1e0-151">Procédure : utiliser des voix prémixées</span><span class="sxs-lookup"><span data-stu-id="6f1e0-151">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="6f1e0-152">Procédure : Créer une chaîne d’effets</span><span class="sxs-lookup"><span data-stu-id="6f1e0-152">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



