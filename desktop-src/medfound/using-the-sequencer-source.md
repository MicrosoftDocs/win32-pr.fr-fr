---
description: Cette rubrique explique comment utiliser la source de Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Utilisation de la source de Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517736"
---
# <a name="using-the-sequencer-source"></a><span data-ttu-id="c50d6-103">Utilisation de la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="c50d6-103">Using the Sequencer Source</span></span>

<span data-ttu-id="c50d6-104">Cette rubrique explique comment utiliser la [source de Sequencer](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="c50d6-104">This topic describes how to use the [Sequencer Source](sequencer-source.md).</span></span> <span data-ttu-id="c50d6-105">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="c50d6-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="c50d6-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="c50d6-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="c50d6-107">Ajout de topologies</span><span class="sxs-lookup"><span data-stu-id="c50d6-107">Adding Topologies</span></span>](#adding-topologies)
-   [<span data-ttu-id="c50d6-108">Suppression de topologies</span><span class="sxs-lookup"><span data-stu-id="c50d6-108">Deleting Topologies</span></span>](#deleting-topologies)
-   [<span data-ttu-id="c50d6-109">Omission à un segment</span><span class="sxs-lookup"><span data-stu-id="c50d6-109">Skipping to a Segment</span></span>](#skipping-to-a-segment)
-   [<span data-ttu-id="c50d6-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c50d6-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="c50d6-111">Pour obtenir une vue d’ensemble générale de la source de Sequencer, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="c50d6-111">For a general overview of the sequencer source, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

## <a name="overview"></a><span data-ttu-id="c50d6-112">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="c50d6-112">Overview</span></span>

<span data-ttu-id="c50d6-113">La source Sequencer expose les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="c50d6-113">The sequencer source exposes the following interfaces.</span></span>



| <span data-ttu-id="c50d6-114">Interface</span><span class="sxs-lookup"><span data-stu-id="c50d6-114">Interface</span></span>                                                                        | <span data-ttu-id="c50d6-115">Description</span><span class="sxs-lookup"><span data-stu-id="c50d6-115">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c50d6-116">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="c50d6-116">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | <span data-ttu-id="c50d6-117">Expose les fonctionnalités de source multimédia génériques.</span><span class="sxs-lookup"><span data-stu-id="c50d6-117">Exposes generic media source functionality.</span></span>                                        |
| [<span data-ttu-id="c50d6-118">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="c50d6-118">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | <span data-ttu-id="c50d6-119">Permet à l’application d’ajouter ou de supprimer des topologies.</span><span class="sxs-lookup"><span data-stu-id="c50d6-119">Enables the application to add or remove topologies.</span></span>                               |
| [<span data-ttu-id="c50d6-120">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="c50d6-120">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | <span data-ttu-id="c50d6-121">Récupère la topologie suivante à partir de la file d’attente de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="c50d6-121">Retrieves the next topology to queue on the Media Session.</span></span>                         |
| [<span data-ttu-id="c50d6-122">**IMFMediaSourcePresentationProvider**</span><span class="sxs-lookup"><span data-stu-id="c50d6-122">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | <span data-ttu-id="c50d6-123">Utilisé par la session multimédia pour terminer les segments.</span><span class="sxs-lookup"><span data-stu-id="c50d6-123">Used by the Media Session to end segments.</span></span> <span data-ttu-id="c50d6-124">Les applications n’utilisent pas cette interface.</span><span class="sxs-lookup"><span data-stu-id="c50d6-124">Applications do not use this interface.</span></span> |
| [<span data-ttu-id="c50d6-125">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="c50d6-125">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | <span data-ttu-id="c50d6-126">Interroge la source de Sequencer pour les [interfaces de service](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c50d6-126">Queries the sequencer source for [Service Interfaces](service-interfaces.md).</span></span>     |



 

<span data-ttu-id="c50d6-127">Pour lire une séquence de sources multimédias, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c50d6-127">To play a sequence of media sources, perform the following steps:</span></span>

1.  <span data-ttu-id="c50d6-128">Pour créer la source de Sequencer, appelez la fonction [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-128">To create the sequencer source, call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function.</span></span>
2.  <span data-ttu-id="c50d6-129">Pour chaque segment, créez une topologie de lecture, comme décrit dans [création de topologies de lecture](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="c50d6-129">For each segment, create a playback topology, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="c50d6-130">Pour ajouter la topologie à la présentation, appelez [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="c50d6-130">To add the topology to the presentation, call [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span>
3.  <span data-ttu-id="c50d6-131">Avant de commencer la lecture, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sur la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c50d6-131">Before starting playback, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the sequencer source.</span></span> <span data-ttu-id="c50d6-132">Cette méthode retourne un pointeur vers un descripteur de présentation pour le premier segment.</span><span class="sxs-lookup"><span data-stu-id="c50d6-132">This method returns a pointer to a presentation descriptor for the first segment.</span></span> <span data-ttu-id="c50d6-133">Pour obtenir la topologie associée à ce segment, appelez **QueryInterface** sur la source de Sequencer pour l’interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-133">To get the topology associated with this segment, call **QueryInterface** on the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span> <span data-ttu-id="c50d6-134">Transmettez le descripteur de présentation à la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-134">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="c50d6-135">Cette méthode retourne un pointeur vers la topologie.</span><span class="sxs-lookup"><span data-stu-id="c50d6-135">This method returns a pointer to the topology.</span></span>
4.  <span data-ttu-id="c50d6-136">Transmettez la topologie du premier segment à la session multimédia, en appelant la méthode [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) de la session de média.</span><span class="sxs-lookup"><span data-stu-id="c50d6-136">Pass the topology for the first segment to the Media Session, by calling the Media Session's [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>
5.  <span data-ttu-id="c50d6-137">Démarrez la lecture en appelant [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="c50d6-137">Start playback by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>
6.  <span data-ttu-id="c50d6-138">Lorsque la source de Sequencer est prête à préparer le segment suivant, elle envoie un événement [MENewPresentation](menewpresentation.md) dont les données d’événement sont un pointeur d’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-138">When the sequencer source is ready to preroll the next segment, it sends an [MENewPresentation](menewpresentation.md) event whose event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface pointer.</span></span> <span data-ttu-id="c50d6-139">Là encore, récupérez la topologie du segment en appelant [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) sur la source de Sequencer et définissez la topologie sur la session de média en appelant [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="c50d6-139">Again, get the topology for the segment by calling [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the sequencer source, and set the topology on the Media Session by calling [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="c50d6-140">Il n’est pas nécessaire de redémarrer la source du média. elle est automatiquement lue jusqu’au segment suivant.</span><span class="sxs-lookup"><span data-stu-id="c50d6-140">It is not necessary to re-start the media source; it will automatically play through to the next segment.</span></span>
7.  <span data-ttu-id="c50d6-141">Avant de quitter l’application, arrêtez la source de Sequencer en appelant [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="c50d6-141">Before the application quits, shut down the sequencer source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>

<span data-ttu-id="c50d6-142">Le code suivant montre comment récupérer la topologie et la définir sur la session multimédia :</span><span class="sxs-lookup"><span data-stu-id="c50d6-142">The following code shows how to get the topology and set it on the Media Session:</span></span>


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="c50d6-143">Pour obtenir un exemple de code complet, consultez Code de l’exemple de code [source Sequencer](sequencer-source-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="c50d6-143">For a complete code example, see [Sequencer Source Example Code](sequencer-source-example-code.md).</span></span>

## <a name="adding-topologies"></a><span data-ttu-id="c50d6-144">Ajout de topologies</span><span class="sxs-lookup"><span data-stu-id="c50d6-144">Adding Topologies</span></span>

<span data-ttu-id="c50d6-145">La source de Sequencer gère deux listes de topologies : la *liste d’entrée* et la *liste de préroll*.</span><span class="sxs-lookup"><span data-stu-id="c50d6-145">The sequencer source maintains two lists of topologies: the *input list* and the *preroll list*.</span></span>

<span data-ttu-id="c50d6-146">La liste d’entrée est une collection de topologies correspondant aux segments de sélection, dans l’ordre dans lequel ils ont été ajoutés par l’application en appelant [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="c50d6-146">The input list is a collection of topologies corresponding to playlist segments, in the order that they were added by the application by calling [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span> <span data-ttu-id="c50d6-147">Cette méthode affecte à chaque topologie un identificateur de *segment* unique du type **MFSequencerElementId**.</span><span class="sxs-lookup"><span data-stu-id="c50d6-147">This method assigns each topology a unique *segment identifier* of the type **MFSequencerElementId**.</span></span> <span data-ttu-id="c50d6-148">L’identificateur de segment est défini en tant qu’attribut pour tous les nœuds de topologie source.</span><span class="sxs-lookup"><span data-stu-id="c50d6-148">The segment identifier is set as an attribute for all source topology nodes.</span></span> <span data-ttu-id="c50d6-149">Une application peut obtenir l’identificateur de segment à partir d’un nœud source à l’aide de l’attribut d' [ \_ \_ \_ ELEMENTID de séquence TOPONODE MF](mf-toponode-sequence-elementid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-149">An application can get the segment identifier from a source node by using the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute.</span></span> <span data-ttu-id="c50d6-150">La liste d’entrée peut avoir des topologies en double si l’application a appelé **AppendTopology** sur la même topologie plusieurs fois. Toutefois, ils sont identifiés par leurs identificateurs de segment uniques.</span><span class="sxs-lookup"><span data-stu-id="c50d6-150">The input list can have duplicate topologies if the application called **AppendTopology** on the same topology more than once; however, they are identified by their unique segment identifiers.</span></span>

<span data-ttu-id="c50d6-151">La liste de préroll est une collection de topologies de liste d’entrée qui ont été initialisées en vue de la lecture.</span><span class="sxs-lookup"><span data-stu-id="c50d6-151">The preroll list is a collection of input list topologies that have been initialized in preparation for playback.</span></span> <span data-ttu-id="c50d6-152">Cela permet à la session de média de passer à la topologie suivante en toute transparence lorsque la topologie Active se termine.</span><span class="sxs-lookup"><span data-stu-id="c50d6-152">This enables the Media Session to transition to the next topology seamlessly when the active topology ends.</span></span> <span data-ttu-id="c50d6-153">L’application ne peut pas ajouter ou supprimer directement des topologies de la liste de préroll ; elle est générée par la source de Sequencer lorsqu’une topologie de la liste d’entrée est sélectionnée pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="c50d6-153">The application cannot directly add or remove topologies from the preroll list; it is generated by the sequencer source when a topology from the input list is selected for playback.</span></span> <span data-ttu-id="c50d6-154">Ainsi, la source de Sequencer ajoute la topologie suivante à partir de la liste d’entrée à la liste des prérolls.</span><span class="sxs-lookup"><span data-stu-id="c50d6-154">This causes the sequencer source to add the next topology from the input list to the preroll list.</span></span> <span data-ttu-id="c50d6-155">Après cela, la source Sequencer déclenche de manière asynchrone l’événement [MENewPresentation](menewpresentation.md) et passe le descripteur de présentation pour la topologie de prérestauration en tant que données d’événement.</span><span class="sxs-lookup"><span data-stu-id="c50d6-155">After doing so, the sequencer source asynchronously raises the [MENewPresentation](menewpresentation.md) event and passes the presentation descriptor for the preroll topology as event data.</span></span> <span data-ttu-id="c50d6-156">L’application doit écouter cet événement à l’aide de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) de la session de média et effectuer la file d’attente de la topologie de prérestauration sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="c50d6-156">The application must listen for this event by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface and queue the preroll topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="c50d6-157">Cette opération doit être effectuée avant que la session multimédia ne termine la lecture de la topologie Active.</span><span class="sxs-lookup"><span data-stu-id="c50d6-157">This must be done before the Media Session completes playback of the active topology.</span></span> <span data-ttu-id="c50d6-158">**SetTopology** informe la session multimédia à propos de la topologie suivante qu’elle doit lire après la fin de la lecture de la topologie Active.</span><span class="sxs-lookup"><span data-stu-id="c50d6-158">**SetTopology** informs the Media Session about the next topology that it must play after playback of the active topology has ended.</span></span> <span data-ttu-id="c50d6-159">Pour garantir un treansition transparent, l’application doit appeler **SetTopology** avant la fin de la session de média en lisant la topologie précédente.</span><span class="sxs-lookup"><span data-stu-id="c50d6-159">To ensure a seamless treansition, the application must call **SetTopology** before the Media Session completes playing the previous topology.</span></span> <span data-ttu-id="c50d6-160">Dans le cas contraire, il y aura un intervalle entre les segments.</span><span class="sxs-lookup"><span data-stu-id="c50d6-160">Otherwise, there will be a gap between the segments.</span></span>

<span data-ttu-id="c50d6-161">L’événement [MENewPresentation](menewpresentation.md) est déclenché tant qu’il existe une topologie qui suit la topologie Active.</span><span class="sxs-lookup"><span data-stu-id="c50d6-161">The [MENewPresentation](menewpresentation.md) event is raised as long as there is a topology following the active topology.</span></span> <span data-ttu-id="c50d6-162">Par conséquent, si la liste d’entrée contient une seule topologie, ou si la topologie Active est la dernière de la liste d’entrée, cet événement n’est pas déclenché.</span><span class="sxs-lookup"><span data-stu-id="c50d6-162">Consequently, if the input list contains only one topology, or if the active topology is the last one in the input list, this event is not raised.</span></span>

<span data-ttu-id="c50d6-163">La liste des prérolls est synchronisée avec la liste d’entrée et est actualisée chaque fois qu’une topologie est ajoutée ou supprimée dans la liste d’entrée.</span><span class="sxs-lookup"><span data-stu-id="c50d6-163">The preroll list is synchronized with the input list and is refreshed each time a topology is added to or deleted from the input list.</span></span>

## <a name="deleting-topologies"></a><span data-ttu-id="c50d6-164">Suppression de topologies</span><span class="sxs-lookup"><span data-stu-id="c50d6-164">Deleting Topologies</span></span>

<span data-ttu-id="c50d6-165">Pour supprimer une topologie de la source de Sequencer, une application doit appeler la méthode [**IMFSequencerSource ::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) et spécifier l’identificateur de segment.</span><span class="sxs-lookup"><span data-stu-id="c50d6-165">To remove a topology from the sequencer source, an application must call the [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) method and specify the segment identifier.</span></span>

<span data-ttu-id="c50d6-166">Avant d’appeler [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), l’application doit s’assurer que la session multimédia n’utilise pas la topologie que l’application souhaite supprimer.</span><span class="sxs-lookup"><span data-stu-id="c50d6-166">Before calling [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), the application must make sure that Media Session is not using the topology that the application wants to delete.</span></span> <span data-ttu-id="c50d6-167">Pour ce faire, les deux conditions suivantes doivent se produire avant que l’application appelle **DeleteTopology**:</span><span class="sxs-lookup"><span data-stu-id="c50d6-167">To do this, both of the following must occur before the application calls **DeleteTopology**:</span></span>

-   <span data-ttu-id="c50d6-168">L’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec MF \_ TOPOSTATUS \_ terminé est reçu pour la topologie pour s’assurer que la lecture de la session multimédia est terminée.</span><span class="sxs-lookup"><span data-stu-id="c50d6-168">[MESessionTopologyStatus](mesessiontopologystatus.md) event with MF\_TOPOSTATUS\_ENDED is received for the topology to ensure that Media Session has completed playback.</span></span>

-   <span data-ttu-id="c50d6-169">[MESessionTopologyStatus](mesessiontopologystatus.md) avec MF \_ TOPOSTATUS \_ Started \_ source est reçu pour la topologie suivante afin de s’assurer que la session multimédia a démarré la prochaine topologie, [MESessionEnded](mesessionended.md) événement est reçu pour s’assurer que la session multimédia est terminée avec la dernière topologie de la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c50d6-169">[MESessionTopologyStatus](mesessiontopologystatus.md) with MF\_TOPOSTATUS\_STARTED\_SOURCE is received for the next topology to ensure that the Media Session has started playing the next topology, [MESessionEnded](mesessionended.md) event is received to ensure that Media Session is done with the last topology in the sequencer source.</span></span>

<span data-ttu-id="c50d6-170">Si le segment en cours de suppression est la topologie Active, la lecture est arrêtée et la source Sequencer déclenche l’événement [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-170">If the segment being deleted is the active topology, playback is stopped and the sequencer source raises the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span> <span data-ttu-id="c50d6-171">Si la topologie Active est également la dernière topologie, l’événement [MEEndOfPresentation](meendofpresentation.md) est déclenché.</span><span class="sxs-lookup"><span data-stu-id="c50d6-171">If the active topology is also the last topology, the [MEEndOfPresentation](meendofpresentation.md) event is raised.</span></span>

## <a name="skipping-to-a-segment"></a><span data-ttu-id="c50d6-172">Omission à un segment</span><span class="sxs-lookup"><span data-stu-id="c50d6-172">Skipping to a Segment</span></span>

<span data-ttu-id="c50d6-173">Une application peut passer à un segment particulier de la séquence en démarrant la [session multimédia](media-session.md) avec un décalage de segment, comme suit :</span><span class="sxs-lookup"><span data-stu-id="c50d6-173">An application can skip to a particular segment in the sequence by starting the [Media Session](media-session.md) with a segment offset, as follows:</span></span>

1.  <span data-ttu-id="c50d6-174">Appelez la fonction [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) pour créer le décalage du segment.</span><span class="sxs-lookup"><span data-stu-id="c50d6-174">Call the [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) function to create the segment offset.</span></span> <span data-ttu-id="c50d6-175">Spécifiez l’identificateur du segment dans le paramètre *dwId* .</span><span class="sxs-lookup"><span data-stu-id="c50d6-175">Specify the identifier of the segment in the *dwId* parameter.</span></span> <span data-ttu-id="c50d6-176">(L’identificateur a été retourné par la méthode [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) lorsque vous avez ajouté la topologie à la source du séquenceur pour la première fois.) Le paramètre *hnsOffset* spécifie un décalage horaire par rapport au début du segment.</span><span class="sxs-lookup"><span data-stu-id="c50d6-176">(The identifier was returned by the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method when you first added the topology to the sequencer source.) The *hnsOffset* parameter specifies a time offset, relative to the start of the segment.</span></span> <span data-ttu-id="c50d6-177">La lecture démarrera à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="c50d6-177">Playback will start at this time.</span></span> <span data-ttu-id="c50d6-178">Pour le paramètre *pvarSegmentOffset* , transmettez l’adresse d’un **PROPVARIANT** vide.</span><span class="sxs-lookup"><span data-stu-id="c50d6-178">For the *pvarSegmentOffset* parameter, pass in the address of an empty **PROPVARIANT**.</span></span> <span data-ttu-id="c50d6-179">Quand la fonction retourne, ce **PROPVARIANT** contient le décalage de segment.</span><span class="sxs-lookup"><span data-stu-id="c50d6-179">When the function returns, this **PROPVARIANT** contains the segment offset.</span></span>

2.  <span data-ttu-id="c50d6-180">Appelez la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="c50d6-180">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method on the Media Session.</span></span> <span data-ttu-id="c50d6-181">Pour le paramètre *pguidTimeFormat* , utilisez la valeur GUID de \_ décalage de segment de format de temps MF \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c50d6-181">For the *pguidTimeFormat* parameter, use the GUID value MF\_TIME\_FORMAT\_SEGMENT\_OFFSET.</span></span> <span data-ttu-id="c50d6-182">Cette valeur indique la recherche par décalage de segment.</span><span class="sxs-lookup"><span data-stu-id="c50d6-182">This value indicates seeking by segment offset.</span></span> <span data-ttu-id="c50d6-183">Pour le paramètre *pvarStartPosition* , transmettez l’adresse du **PROPVARIANT** créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="c50d6-183">For the *pvarStartPosition* parameter, pass the address of the **PROPVARIANT** created in the previous step.</span></span>

<span data-ttu-id="c50d6-184">L’exemple de code suivant montre comment passer au début d’un segment spécifié dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="c50d6-184">The following code example shows how to skip to the start of a specified segment in a sequence.</span></span>


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="c50d6-185">Lorsque l’application recherche sur des segments, elle reçoit plusieurs événements, car la source de Sequencer termine le segment actuel et prépare la lecture du nouveau segment.</span><span class="sxs-lookup"><span data-stu-id="c50d6-185">When the application seeks across segments, the application receives several events as the sequencer source ends the current segment and prepares to play the new segment.</span></span> <span data-ttu-id="c50d6-186">Comme ces événements sont reçus de manière asynchrone, il est difficile de prédire la séquence exacte d’événements.</span><span class="sxs-lookup"><span data-stu-id="c50d6-186">Because these events are received asynchronously, it is difficult to predict the exact sequence of events.</span></span> <span data-ttu-id="c50d6-187">Ces événements sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="c50d6-187">These events are as follows:</span></span>

-   <span data-ttu-id="c50d6-188">La source Sequencer envoie un événement [MENewPresentation](menewpresentation.md) pour le nouveau segment vers lequel la session multimédia est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c50d6-188">The sequencer source sends an [MENewPresentation](menewpresentation.md) event for the new segment to which the Media Session is skipping.</span></span>

-   <span data-ttu-id="c50d6-189">Lorsque la source de Sequencer termine le segment actif, elle envoie l’événement [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-189">When the sequencer source ends the active segment, it sends the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span>
-   <span data-ttu-id="c50d6-190">La source de Sequencer annule ensuite la topologie de prérestauration.</span><span class="sxs-lookup"><span data-stu-id="c50d6-190">The sequencer source then cancels the preroll topology.</span></span> <span data-ttu-id="c50d6-191">Cela génère les événements suivants pour la topologie annulée :</span><span class="sxs-lookup"><span data-stu-id="c50d6-191">This results in the following events for the canceled topology:</span></span>

    -   <span data-ttu-id="c50d6-192">Événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec l' \_ \_ indicateur prêt TOPOSTATUS Ready.</span><span class="sxs-lookup"><span data-stu-id="c50d6-192">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span>
    -   <span data-ttu-id="c50d6-193">Événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec l' \_ \_ indicateur source démarré MF TOPOSTATUS \_ .</span><span class="sxs-lookup"><span data-stu-id="c50d6-193">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_STARTED\_SOURCE flag.</span></span>
    -   <span data-ttu-id="c50d6-194">Événement [MEEndOfPresentationSegment](meendofpresentationsegment.md) avec l’attribut de l’annulation de la topologie de la source de l' [ \_ événement \_ \_ \_ MF](mf-event-source-topology-canceled-attribute.md) pour indiquer que la topologie a été annulée par la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c50d6-194">[MEEndOfPresentationSegment](meendofpresentationsegment.md) event with the [MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED](mf-event-source-topology-canceled-attribute.md) attribute to indicate that the topology was canceled by the sequencer source.</span></span>

-   <span data-ttu-id="c50d6-195">Ensuite, la source Sequencer envoie des événements pour le nouveau segment, y compris divers événements [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="c50d6-195">Next, the sequencer source sends events for the new segment, including various [MESessionTopologyStatus](mesessiontopologystatus.md) events.</span></span>
-   <span data-ttu-id="c50d6-196">Si le nouveau segment n’est pas le dernier dans la liste, la source de Sequencer actualise la liste des préroll et déclenche un autre [MENewPresentation](menewpresentation.md) pour la nouvelle topologie de préroll.</span><span class="sxs-lookup"><span data-stu-id="c50d6-196">If the new segment is not the last on the list, the sequencer source refreshes the preroll list and raises another [MENewPresentation](menewpresentation.md) for the new preroll topology.</span></span> <span data-ttu-id="c50d6-197">Pour plus d’informations sur les topologies dans la liste des préroll, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="c50d6-197">For information about topologies in the preroll list, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="c50d6-198">Vous trouverez plus de détails sur les événements envoyés par la source de Sequencer dans la rubrique [événements](sequencer-source-events.md)de la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="c50d6-198">More details about the events sent by the sequencer source can be found in the topic [Sequencer Source Events](sequencer-source-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c50d6-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c50d6-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c50d6-200">Comment créer une sélection</span><span class="sxs-lookup"><span data-stu-id="c50d6-200">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="c50d6-201">Source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="c50d6-201">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



