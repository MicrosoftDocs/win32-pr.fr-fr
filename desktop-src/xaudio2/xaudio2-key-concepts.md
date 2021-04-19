---
description: Cette vue d’ensemble présente des concepts clés pour l’utilisation de XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Concepts clés de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523413"
---
# <a name="xaudio2-key-concepts"></a><span data-ttu-id="d3988-103">Concepts clés de XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3988-103">XAudio2 Key Concepts</span></span>

<span data-ttu-id="d3988-104">Cette vue d’ensemble présente des concepts clés pour l’utilisation de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="d3988-104">This overview introduces some key concepts for using XAudio2.</span></span>

-   [<span data-ttu-id="d3988-105">Moteur XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3988-105">XAudio2 Engine</span></span>](#xaudio2-engine)
-   [<span data-ttu-id="d3988-106">Voix</span><span class="sxs-lookup"><span data-stu-id="d3988-106">Voices</span></span>](#voices)
-   [<span data-ttu-id="d3988-107">Graphique audio</span><span class="sxs-lookup"><span data-stu-id="d3988-107">Audio Graph</span></span>](#audio-graph)
-   [<span data-ttu-id="d3988-108">Rappels</span><span class="sxs-lookup"><span data-stu-id="d3988-108">Callbacks</span></span>](#callbacks)
-   [<span data-ttu-id="d3988-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3988-109">Related Topics</span></span>](#related-topics)

## <a name="xaudio2-engine"></a><span data-ttu-id="d3988-110">Moteur XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3988-110">XAudio2 Engine</span></span>

<span data-ttu-id="d3988-111">L’interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) est au cœur du moteur XAudio2.</span><span class="sxs-lookup"><span data-stu-id="d3988-111">The [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface is the core of the XAudio2 engine.</span></span> <span data-ttu-id="d3988-112">La création d’une instance de l’interface **IXAudio2** permet au client d’énumérer les périphériques audio disponibles, de configurer les propriétés de l’API globale, de créer des voix et de surveiller les performances.</span><span class="sxs-lookup"><span data-stu-id="d3988-112">Creating an instance of the **IXAudio2** interface allows the client to enumerate the available audio devices, to configure global API properties, to create voices, and to monitor performance.</span></span> <span data-ttu-id="d3988-113">La fonction d’assistance [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) effectue des tâches d’instanciation et d’initialisation pour XAudio2.</span><span class="sxs-lookup"><span data-stu-id="d3988-113">The [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper function performs instantiation and initialization tasks for XAudio2.</span></span>

<span data-ttu-id="d3988-114">Vous pouvez créer des instances de XAudio2 plusieurs fois dans un même processus.</span><span class="sxs-lookup"><span data-stu-id="d3988-114">You can create instances of XAudio2 multiple times within a single process.</span></span> <span data-ttu-id="d3988-115">Chaque objet XAudio2 fonctionne de façon indépendante et possède son propre thread de traitement audio.</span><span class="sxs-lookup"><span data-stu-id="d3988-115">Each XAudio2 object operates independently, and has its own audio processing thread.</span></span> <span data-ttu-id="d3988-116">Seuls les paramètres de débogage sont partagés.</span><span class="sxs-lookup"><span data-stu-id="d3988-116">Only the debug settings are shared.</span></span> <span data-ttu-id="d3988-117">Cela est important sur Windows où plusieurs composants différents peuvent être chargés dans un même processus.</span><span class="sxs-lookup"><span data-stu-id="d3988-117">This is important on Windows where several different components may be loaded in a single process.</span></span> <span data-ttu-id="d3988-118">Par exemple, Internet Explorer peut utiliser plusieurs composants XAudio2 simultanément.</span><span class="sxs-lookup"><span data-stu-id="d3988-118">For example, Internet Explorer might use multiple XAudio2 components simultaneously.</span></span> <span data-ttu-id="d3988-119">Bien qu’il soit possible de créer plusieurs objets de moteur XAudio2 dans une même application cliente, vous ne devez pas transmettre des informations entre leurs graphiques respectifs.</span><span class="sxs-lookup"><span data-stu-id="d3988-119">Although it is possible to create multiple XAudio2 engine objects within a single client application, you should not pass information between their respective graphs.</span></span>

<span data-ttu-id="d3988-120">Pour obtenir un exemple d’initialisation du moteur XAudio2, consultez [How to : Initialize XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="d3988-120">For an example of initializing the XAudio2 engine, see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>

## <a name="voices"></a><span data-ttu-id="d3988-121">Voix</span><span class="sxs-lookup"><span data-stu-id="d3988-121">Voices</span></span>

<span data-ttu-id="d3988-122">Les voix sont les objets utilisés par XAudio2 pour traiter, manipuler et lire des données audio.</span><span class="sxs-lookup"><span data-stu-id="d3988-122">Voices are the objects XAudio2 use to process, to manipulate, and to play audio data.</span></span> <span data-ttu-id="d3988-123">Il existe trois types de voix dans XAudio2.</span><span class="sxs-lookup"><span data-stu-id="d3988-123">There are three types of voices in XAudio2.</span></span>

-   [<span data-ttu-id="d3988-124">**Voix source**</span><span class="sxs-lookup"><span data-stu-id="d3988-124">**Source Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    <span data-ttu-id="d3988-125">Les voix source représentent un flux de données audio.</span><span class="sxs-lookup"><span data-stu-id="d3988-125">Source voices represent a stream of audio data.</span></span> <span data-ttu-id="d3988-126">Les voix source envoient leurs données à d’autres types de voix.</span><span class="sxs-lookup"><span data-stu-id="d3988-126">Source voices send their data to other types of voices.</span></span>

-   [<span data-ttu-id="d3988-127">**Voix de mixage secondaire**</span><span class="sxs-lookup"><span data-stu-id="d3988-127">**Submix Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    <span data-ttu-id="d3988-128">Les voix de mixage secondaire effectuent une manipulation des données audio qu’elles reçoivent.</span><span class="sxs-lookup"><span data-stu-id="d3988-128">Submix voices perform some manipulation of audio data they receive.</span></span> <span data-ttu-id="d3988-129">Un exemple de manipulation de données audio peut être une conversion de taux d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="d3988-129">One example of audio data manipulation might be sample rate conversion.</span></span> <span data-ttu-id="d3988-130">Une fois qu’une voix de mixage a traité des données, elle les transmet à une autre voix de mixage ou à une voix principale.</span><span class="sxs-lookup"><span data-stu-id="d3988-130">After a submix voice processes data, it passes that data to another submix voice or to a master voice.</span></span>

-   [<span data-ttu-id="d3988-131">**Mastérisation des voix**</span><span class="sxs-lookup"><span data-stu-id="d3988-131">**Mastering Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    <span data-ttu-id="d3988-132">La maîtrise des voix reçoit des données des voix et des voix de mixage source et envoie ces données au matériel audio.</span><span class="sxs-lookup"><span data-stu-id="d3988-132">Mastering voices receive data from source voices and submix voices, and sends that data to the audio hardware.</span></span>

<span data-ttu-id="d3988-133">Pour obtenir une vue d’ensemble des voix XAudio2, consultez [XAudio2 Voices](voices.md) .</span><span class="sxs-lookup"><span data-stu-id="d3988-133">See [XAudio2 Voices](voices.md) for an overview of XAudio2 voices.</span></span>

## <a name="audio-graph"></a><span data-ttu-id="d3988-134">Graphique audio</span><span class="sxs-lookup"><span data-stu-id="d3988-134">Audio Graph</span></span>

<span data-ttu-id="d3988-135">Un graphique audio est une collection de voix XAudio2.</span><span class="sxs-lookup"><span data-stu-id="d3988-135">An audio graph is a collection of XAudio2 voices.</span></span> <span data-ttu-id="d3988-136">L’audio commence à un côté d’un graphique audio dans les voix source, passe éventuellement par une ou plusieurs voix de mixage et se termine à une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="d3988-136">Audio starts at one side of an audio graph in source voices, optionally passes through one or more submix voices, and ends at a mastering voice.</span></span> <span data-ttu-id="d3988-137">Un graphique audio contient une voix source pour chaque son en cours de lecture, zéro, une ou plusieurs voix de mixage et une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="d3988-137">An audio graph will contain a source voice for each sound currently playing, zero or more submix voices, and one mastering voice.</span></span> <span data-ttu-id="d3988-138">Le graphique audio le plus simple, et le minimum nécessaire pour faire un bruit dans XAudio2, est une seule voix source qui s’effectue directement sur une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="d3988-138">The simplest audio graph, and the minimum needed to make a noise in XAudio2, is a single source voice outputting directly to a mastering voice.</span></span> <span data-ttu-id="d3988-139">Consultez [Comment : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md) pour obtenir un exemple des étapes minimales nécessaires pour lire un son avec XAudio2.</span><span class="sxs-lookup"><span data-stu-id="d3988-139">See [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md) for an example of the minimum steps need to play a sound with XAudio2.</span></span>

<span data-ttu-id="d3988-140">Pour obtenir une vue d’ensemble des graphiques audio XAudio2, consultez [XAudio2 audio Graph](audio-graphs.md) .</span><span class="sxs-lookup"><span data-stu-id="d3988-140">See [XAudio2 Audio Graph](audio-graphs.md) for an overview of XAudio2 audio graphs.</span></span>

## <a name="callbacks"></a><span data-ttu-id="d3988-141">Rappels</span><span class="sxs-lookup"><span data-stu-id="d3988-141">Callbacks</span></span>

<span data-ttu-id="d3988-142">Les rappels sont le mécanisme utilisé par XAudio2 pour signaler au code client qu’un événement s’est produit dans une voix ou dans l’objet moteur.</span><span class="sxs-lookup"><span data-stu-id="d3988-142">Callbacks are the mechanism XAudio2 uses to signal client code that some event has occurred in a voice or in the engine object.</span></span> <span data-ttu-id="d3988-143">Étant donné que la lecture audio est asynchrone dans le moteur XAudio2, les rappels fournissent le seul moyen de déterminer à quel moment un son est terminé.</span><span class="sxs-lookup"><span data-stu-id="d3988-143">Because audio playback is asynchronous in the XAudio2 engine, callbacks provide the only way to determine when a sound is finished playing.</span></span>

<span data-ttu-id="d3988-144">Pour obtenir une vue d’ensemble des rappels XAudio2, consultez [rappels XAudio2](callbacks.md) .</span><span class="sxs-lookup"><span data-stu-id="d3988-144">See [XAudio2 Callbacks](callbacks.md) for an overview of XAudio2 callbacks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3988-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3988-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3988-146">Prise en main</span><span class="sxs-lookup"><span data-stu-id="d3988-146">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="d3988-147">Versions de XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3988-147">XAudio2 Versions</span></span>](xaudio2-versions.md)
</dt> <dt>

[<span data-ttu-id="d3988-148">Procédure : initialiser XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3988-148">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="d3988-149">Comment : lire un son avec XAudio2</span><span class="sxs-lookup"><span data-stu-id="d3988-149">How to: Play a sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



