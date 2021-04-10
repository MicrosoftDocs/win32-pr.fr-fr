---
description: Cette vue d’ensemble introduit plusieurs méthodes XAudio2 que vous pouvez appeler dans le cadre d’un ensemble d’opérations.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Ensembles d’opérations XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210801"
---
# <a name="xaudio2-operation-sets"></a><span data-ttu-id="69ba3-103">Ensembles d’opérations XAudio2</span><span class="sxs-lookup"><span data-stu-id="69ba3-103">XAudio2 Operation Sets</span></span>

<span data-ttu-id="69ba3-104">Cette vue d’ensemble introduit plusieurs méthodes XAudio2 que vous pouvez appeler dans le cadre d’un ensemble d’opérations.</span><span class="sxs-lookup"><span data-stu-id="69ba3-104">This overview introduces several XAudio2 methods that you can call as part of an operation set.</span></span>

<span data-ttu-id="69ba3-105">Plusieurs méthodes XAudio2 prennent l’argument *OperationSet* , ce qui leur permet d’être appelés dans le cadre d’un groupe différé.</span><span class="sxs-lookup"><span data-stu-id="69ba3-105">Several XAudio2 methods take the *OperationSet* argument, which allows them to be called as part of a deferred group.</span></span> <span data-ttu-id="69ba3-106">À un moment donné, vous pouvez appliquer un ensemble complet de modifications simultanément en appelant la fonction [**IXAudio2 :: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec l’identificateur *OperationSet* pour ce groupe.</span><span class="sxs-lookup"><span data-stu-id="69ba3-106">At a specific time, you can apply an entire set of changes simultaneously by calling the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the *OperationSet* identifier for that group.</span></span> <span data-ttu-id="69ba3-107">L’identificateur est un nombre arbitraire.</span><span class="sxs-lookup"><span data-stu-id="69ba3-107">The identifier is an arbitrary number.</span></span> <span data-ttu-id="69ba3-108">Par conséquent, il permet à des parties distinctes du code client d’appliquer des modifications atomiques distinctes au graphique sans aucun conflit.</span><span class="sxs-lookup"><span data-stu-id="69ba3-108">Thus, it allows separate parts of the client code to apply separate atomic changes to the graph without any conflict.</span></span> <span data-ttu-id="69ba3-109">La pratique recommandée consiste à ce que le client incrémente un compteur global chaque fois qu’il doit générer un nouvel identificateur *OperationSet* unique.</span><span class="sxs-lookup"><span data-stu-id="69ba3-109">The recommended practice is for the client to increment a global counter whenever it needs to generate a unique, new *OperationSet* identifier.</span></span> <span data-ttu-id="69ba3-110">Un ensemble de modifications apportées au graphique, appliqué atomiquement, est garanti comme étant exact.</span><span class="sxs-lookup"><span data-stu-id="69ba3-110">A set of changes to the graph, applied atomically, is guaranteed to be sample-accurate.</span></span> <span data-ttu-id="69ba3-111">Par exemple, les voix commencent à se synchroniser.</span><span class="sxs-lookup"><span data-stu-id="69ba3-111">For example, voices will start in sync.</span></span>

<span data-ttu-id="69ba3-112">Si vous affectez à *OperationSet* la valeur XAUDIO2 \_ Commit \_ Now, la modification s’applique immédiatement.</span><span class="sxs-lookup"><span data-stu-id="69ba3-112">If you set *OperationSet* to XAUDIO2\_COMMIT\_NOW, the change applies immediately.</span></span> <span data-ttu-id="69ba3-113">Elle prend effet lors de la première passe de traitement audio après l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="69ba3-113">It takes effect in the first audio processing pass after the method call.</span></span> <span data-ttu-id="69ba3-114">Si vous appelez [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec XAUDIO2 \_ Commit \_ All, les modifications apportées à tous les ensembles d’opérations en attente sont effectuées, quel que soit leur identificateur *OperationSet* .</span><span class="sxs-lookup"><span data-stu-id="69ba3-114">If you call [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2\_COMMIT\_ALL, changes to all pending operations sets are performed, regardless of their *OperationSet* identifier.</span></span>

<span data-ttu-id="69ba3-115">Certaines méthodes prennent effet immédiatement quand elles sont appelées à partir d’un rappel XAudio2 avec un *OperationSet* de XAudio2 \_ valider \_ maintenant.</span><span class="sxs-lookup"><span data-stu-id="69ba3-115">Certain methods take effect immediately when they are called from an XAudio2 callback with an *OperationSet* of XAUDIO2\_COMMIT\_NOW.</span></span> <span data-ttu-id="69ba3-116">Toutes les autres méthodes qui acceptent un argument *OperationSet* prennent effet uniquement lors du prochain passage de traitement après l’appel de la méthode (si elle est appelée avec XAUDIO2 \_ Commit \_ Now) ou après l’appel de [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) avec le même *OperationSet*.</span><span class="sxs-lookup"><span data-stu-id="69ba3-116">All other methods that take an *OperationSet* argument only take effect on the next processing pass after the method is called (if called with XAUDIO2\_COMMIT\_NOW), or after [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) is called with the same *OperationSet*.</span></span> <span data-ttu-id="69ba3-117">Pour cette raison, certains appels de méthode peuvent ne pas se produire toujours dans le même ordre que celui dans lequel ils ont été appelés.</span><span class="sxs-lookup"><span data-stu-id="69ba3-117">Because of this, certain method calls may not always happen in the same order in which they were called.</span></span>

<span data-ttu-id="69ba3-118">Toutes les opérations en attente sont validées atomiquement lors de l’appel de [**IXAudio2 :: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) .</span><span class="sxs-lookup"><span data-stu-id="69ba3-118">All pending operations are committed atomically when [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) is called.</span></span> <span data-ttu-id="69ba3-119">Toutes les méthodes qui sont appelées pendant que le moteur est arrêté prennent effet immédiatement, quelle que soit la valeur *OperationSet* fournie.</span><span class="sxs-lookup"><span data-stu-id="69ba3-119">Any methods that are called while the engine is stopped take effect immediately, regardless of the *OperationSet* value provided.</span></span> <span data-ttu-id="69ba3-120">Lorsque vous redémarrez le moteur, XAudio2 revient en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="69ba3-120">When you restart the engine, XAudio2 returns to asynchronous mode.</span></span>

<span data-ttu-id="69ba3-121">Les scénarios les plus simples dans lesquels les ensembles d’opérations sont utiles incluent les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="69ba3-121">Simple scenarios in which operation sets are useful include the following examples.</span></span>

-   <span data-ttu-id="69ba3-122">Démarrage simultané de plusieurs voix.</span><span class="sxs-lookup"><span data-stu-id="69ba3-122">Starting multiple voices simultaneously.</span></span>
-   <span data-ttu-id="69ba3-123">Envoi simultané d’une mémoire tampon à une voix, définition des paramètres vocaux et démarrage de la voix.</span><span class="sxs-lookup"><span data-stu-id="69ba3-123">Simultaneously submitting a buffer to a voice, setting the voice parameters, and starting the voice.</span></span>
-   <span data-ttu-id="69ba3-124">En effectuant une modification à grande échelle du graphique, par exemple en connectant toutes les voix source à une nouvelle voix de mixage.</span><span class="sxs-lookup"><span data-stu-id="69ba3-124">Making a large-scale change to the graph, such as connecting all source voices to a new submix voice.</span></span>

<span data-ttu-id="69ba3-125">Consultez [Comment : regrouper des méthodes audio comme une opération définie](how-to--group-audio-methods-as-an-operation-set.md) pour obtenir un exemple d’utilisation d’un jeu d’opérations.</span><span class="sxs-lookup"><span data-stu-id="69ba3-125">See [How to: Group Audio Methods as an Operation Set](how-to--group-audio-methods-as-an-operation-set.md) for an example of using an operation set.</span></span>

## <a name="operation-set-methods"></a><span data-ttu-id="69ba3-126">Méthodes de définition d’opérations</span><span class="sxs-lookup"><span data-stu-id="69ba3-126">Operation Set Methods</span></span>

<span data-ttu-id="69ba3-127">Vous pouvez appeler les méthodes suivantes dans le cadre d’un ensemble d’opérations.</span><span class="sxs-lookup"><span data-stu-id="69ba3-127">You can call the following methods as part of an operation set.</span></span>

-   [<span data-ttu-id="69ba3-128">**IXAudio2SourceVoice :: ExitLoop**</span><span class="sxs-lookup"><span data-stu-id="69ba3-128">**IXAudio2SourceVoice::ExitLoop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [<span data-ttu-id="69ba3-129">**IXAudio2Voice::SetFilterParameters**</span><span class="sxs-lookup"><span data-stu-id="69ba3-129">**IXAudio2Voice::SetFilterParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [<span data-ttu-id="69ba3-130">**IXAudio2SourceVoice :: SetFrequencyRatio**</span><span class="sxs-lookup"><span data-stu-id="69ba3-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [<span data-ttu-id="69ba3-131">**IXAudio2Voice ::D isableEffect**</span><span class="sxs-lookup"><span data-stu-id="69ba3-131">**IXAudio2Voice::DisableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [<span data-ttu-id="69ba3-132">**IXAudio2Voice::EnableEffect**</span><span class="sxs-lookup"><span data-stu-id="69ba3-132">**IXAudio2Voice::EnableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [<span data-ttu-id="69ba3-133">**IXAudio2Voice::SetChannelVolumes**</span><span class="sxs-lookup"><span data-stu-id="69ba3-133">**IXAudio2Voice::SetChannelVolumes**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [<span data-ttu-id="69ba3-134">**IXAudio2Voice::SetEffectParameters**</span><span class="sxs-lookup"><span data-stu-id="69ba3-134">**IXAudio2Voice::SetEffectParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [<span data-ttu-id="69ba3-135">**IXAudio2Voice::SetOutputMatrix**</span><span class="sxs-lookup"><span data-stu-id="69ba3-135">**IXAudio2Voice::SetOutputMatrix**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [<span data-ttu-id="69ba3-136">**IXAudio2Voice::SetVolume**</span><span class="sxs-lookup"><span data-stu-id="69ba3-136">**IXAudio2Voice::SetVolume**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [<span data-ttu-id="69ba3-137">**IXAudio2SourceVoice :: Start**</span><span class="sxs-lookup"><span data-stu-id="69ba3-137">**IXAudio2SourceVoice::Start**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [<span data-ttu-id="69ba3-138">**IXAudio2SourceVoice :: Stop**</span><span class="sxs-lookup"><span data-stu-id="69ba3-138">**IXAudio2SourceVoice::Stop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

<span data-ttu-id="69ba3-139">Comme décrit précédemment, le code client doit finalement appeler la fonction [**IXAudio2 :: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) pour exécuter les modifications différées.</span><span class="sxs-lookup"><span data-stu-id="69ba3-139">As described previously, client code must ultimately call the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) to execute the deferred changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69ba3-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69ba3-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69ba3-141">Ensembles d’opérations</span><span class="sxs-lookup"><span data-stu-id="69ba3-141">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="69ba3-142">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="69ba3-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="69ba3-143">Procédure : regrouper des méthodes audio comme un ensemble d’opérations</span><span class="sxs-lookup"><span data-stu-id="69ba3-143">How to: Group Audio Methods as an Operation Set</span></span>](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
