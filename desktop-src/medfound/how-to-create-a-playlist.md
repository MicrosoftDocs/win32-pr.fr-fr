---
description: Cette rubrique explique comment utiliser la source de séquence pour lire une séquence de fichiers.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Comment créer une sélection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527688"
---
# <a name="how-to-create-a-playlist"></a><span data-ttu-id="fbefa-103">Comment créer une sélection</span><span class="sxs-lookup"><span data-stu-id="fbefa-103">How to Create a Playlist</span></span>

<span data-ttu-id="fbefa-104">Cette rubrique explique comment utiliser la source de séquence pour lire une séquence de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fbefa-104">This topic describes how to use the Sequence Source to play a sequence of files.</span></span>

## <a name="overview"></a><span data-ttu-id="fbefa-105">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="fbefa-105">Overview</span></span>

<span data-ttu-id="fbefa-106">Pour lire des fichiers multimédias dans une séquence, l’application doit ajouter des topologies dans une séquence afin de créer une sélection, puis les faire défiler sur la session multimédia pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="fbefa-106">To play media files in a sequence, the application must add topologies in a sequence to create a playlist, and queue these topologies on the Media Session for playback.</span></span>

<span data-ttu-id="fbefa-107">La source de Sequencer garantit une lecture transparente en initialisant et en chargeant la topologie suivante avant que la session multimédia ne commence à lire la topologie actuelle.</span><span class="sxs-lookup"><span data-stu-id="fbefa-107">The sequencer source ensures seamless playback by initializing and loading the next topology before the Media Session starts playing the current topology.</span></span> <span data-ttu-id="fbefa-108">Cela permet à l’application de démarrer rapidement la topologie suivante chaque fois qu’elle est requise.</span><span class="sxs-lookup"><span data-stu-id="fbefa-108">This enables the application to start the next topology quickly whenever it is required.</span></span>

<span data-ttu-id="fbefa-109">La session multimédia est responsable de l’alimentation des données aux récepteurs et de la diffusion des topologies dans la source de séquence.</span><span class="sxs-lookup"><span data-stu-id="fbefa-109">The Media Session is responsible for feeding data to the sinks and playing the topologies in the sequence source.</span></span> <span data-ttu-id="fbefa-110">En outre, la session multimédia gère l’heure de présentation des segments.</span><span class="sxs-lookup"><span data-stu-id="fbefa-110">In addition, the Media Session manages the presentation time for the segments.</span></span>

<span data-ttu-id="fbefa-111">Pour plus d’informations sur la façon dont la source Sequencer gère les topologies, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-111">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="fbefa-112">Cette procédure pas à pas contient les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fbefa-112">This walk-through contains the following steps:</span></span>

1.  [<span data-ttu-id="fbefa-113">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="fbefa-113">Prerequisites</span></span>](#prerequisites)
2.  [<span data-ttu-id="fbefa-114">Initialisation de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbefa-114">Initializing Media Foundation</span></span>](#initializing-media-foundation)
3.  [<span data-ttu-id="fbefa-115">Création d’objets Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbefa-115">Creating Media Foundation Objects</span></span>](#creating-media-foundation-objects)
4.  [<span data-ttu-id="fbefa-116">Création de la source du média</span><span class="sxs-lookup"><span data-stu-id="fbefa-116">Creating the Media Source</span></span>](#creating-the-media-source)
5.  [<span data-ttu-id="fbefa-117">Création de topologies partielles</span><span class="sxs-lookup"><span data-stu-id="fbefa-117">Creating Partial Topologies</span></span>](#creating-partial-topologies)
6.  [<span data-ttu-id="fbefa-118">Ajout de topologies à la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="fbefa-118">Adding Topologies to the Sequencer Source</span></span>](#adding-topologies-to-the-sequencer-source)
7.  [<span data-ttu-id="fbefa-119">Définition de la première topologie sur la session multimédia</span><span class="sxs-lookup"><span data-stu-id="fbefa-119">Setting the First Topology on the Media Session</span></span>](#setting-the-first-topology-on-the-media-session)
8.  [<span data-ttu-id="fbefa-120">Mise en file d’attente de la topologie suivante sur la session multimédia</span><span class="sxs-lookup"><span data-stu-id="fbefa-120">Queuing the Next Topology on the Media Session</span></span>](#queuing-the-next-topology-on-the-media-session)
9.  [<span data-ttu-id="fbefa-121">Libération de la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="fbefa-121">Releasing the Sequencer Source</span></span>](#releasing-the-sequencer-source)

<span data-ttu-id="fbefa-122">Les exemples de code présentés dans cette rubrique sont des extraits de l' [exemple de code source Sequencer](sequencer-source-example-code.md), qui contient l’exemple de code complet.</span><span class="sxs-lookup"><span data-stu-id="fbefa-122">The code examples shown this topic are excerpts from the topic [Sequencer Source Example Code](sequencer-source-example-code.md), which contains the complete example code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fbefa-123">Prérequis</span><span class="sxs-lookup"><span data-stu-id="fbefa-123">Prerequisites</span></span>

<span data-ttu-id="fbefa-124">Avant de commencer cette procédure pas à pas, familiarisez-vous avec les concepts de Media Foundation suivants :</span><span class="sxs-lookup"><span data-stu-id="fbefa-124">Before starting this walk-through, familiarize yourself with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="fbefa-125">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="fbefa-125">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="fbefa-126">Topologies</span><span class="sxs-lookup"><span data-stu-id="fbefa-126">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="fbefa-127">Générateurs d’événements de média</span><span class="sxs-lookup"><span data-stu-id="fbefa-127">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="fbefa-128">Descripteurs de présentation</span><span class="sxs-lookup"><span data-stu-id="fbefa-128">Presentation Descriptors</span></span>](presentation-descriptors.md)

<span data-ttu-id="fbefa-129">Lisez également [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md), car l’exemple de code shwon ici s’étend sur le code de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="fbefa-129">Also read [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), because the example code shwon here expands on the code in that topic.</span></span>

## <a name="initializing-media-foundation"></a><span data-ttu-id="fbefa-130">Initialisation de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbefa-130">Initializing Media Foundation</span></span>

<span data-ttu-id="fbefa-131">Avant de pouvoir utiliser des interfaces ou des méthodes Media Foundation, initialisez Media Foundation en appelant la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-131">Before you can use any Media Foundation interfaces or methods, initialize Media Foundation by calling the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="fbefa-132">Pour plus d’informations, consultez [initialisation des Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-132">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a><span data-ttu-id="fbefa-133">Création d’objets Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fbefa-133">Creating Media Foundation Objects</span></span>

<span data-ttu-id="fbefa-134">Créez ensuite les objets Media Foundation suivants :</span><span class="sxs-lookup"><span data-stu-id="fbefa-134">Next, create the following Media Foundation objects:</span></span>

-   <span data-ttu-id="fbefa-135">Session multimédia.</span><span class="sxs-lookup"><span data-stu-id="fbefa-135">Media session.</span></span> <span data-ttu-id="fbefa-136">Cet objet expose l’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , qui fournit des méthodes pour lire, suspendre et arrêter la topologie actuelle.</span><span class="sxs-lookup"><span data-stu-id="fbefa-136">This object exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface, which provides methods to play, pause, and stop the current topology.</span></span>
-   <span data-ttu-id="fbefa-137">Source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fbefa-137">Sequencer source.</span></span> <span data-ttu-id="fbefa-138">Cet objet expose l’interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , qui fournit des méthodes pour ajouter, mettre à jour et supprimer des topologies dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="fbefa-138">This object exposes the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface, which provides methods to add, update, and delete topologies in a sequence.</span></span>

1.  <span data-ttu-id="fbefa-139">Appelez la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="fbefa-139">Call the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function to create the Media Session.</span></span>
2.  <span data-ttu-id="fbefa-140">Appelez [**IMFMediaEventQueue :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) pour demander le premier événement de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="fbefa-140">Call [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) to request the first event from the Media Session.</span></span>
3.  <span data-ttu-id="fbefa-141">Appelez la fonction [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) pour créer la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fbefa-141">Call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function to create the sequencer source.</span></span>

<span data-ttu-id="fbefa-142">Le code suivant crée la session multimédia et demande le premier événement :</span><span class="sxs-lookup"><span data-stu-id="fbefa-142">The following code creates the Media Session and requests the first event:</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a><span data-ttu-id="fbefa-143">Création de la source du média</span><span class="sxs-lookup"><span data-stu-id="fbefa-143">Creating the Media Source</span></span>

<span data-ttu-id="fbefa-144">Ensuite, créez une source de média pour le premier segment de sélection.</span><span class="sxs-lookup"><span data-stu-id="fbefa-144">Next, create a media source for the first playlist segment.</span></span> <span data-ttu-id="fbefa-145">Utilisez le programme de [résolution source](source-resolver.md) pour créer une source de média à partir d’une URL.</span><span class="sxs-lookup"><span data-stu-id="fbefa-145">Use the [Source Resolver](source-resolver.md) to create a media source from a URL.</span></span> <span data-ttu-id="fbefa-146">Pour ce faire, appelez la fonction [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) pour créer un programme de résolution source, puis appelez la méthode [**IMFSourceResolver :: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) pour créer la source du média.</span><span class="sxs-lookup"><span data-stu-id="fbefa-146">To do this, call the [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) function to create a source resolver and then call the [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method to create the media source.</span></span>

<span data-ttu-id="fbefa-147">Pour plus d’informations sur les sources multimédias, consultez [sources multimédias](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-147">For information about media sources, see [Media Sources](media-sources.md).</span></span>

## <a name="creating-partial-topologies"></a><span data-ttu-id="fbefa-148">Création de topologies partielles</span><span class="sxs-lookup"><span data-stu-id="fbefa-148">Creating Partial Topologies</span></span>

<span data-ttu-id="fbefa-149">Chaque segment de la source Sequencer a sa propre topologie partielle.</span><span class="sxs-lookup"><span data-stu-id="fbefa-149">Each segment in the sequencer source has its own partial topology.</span></span> <span data-ttu-id="fbefa-150">Ensuite, créez des topologies partielles pour les sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="fbefa-150">Next, create partial topologies for media sources.</span></span> <span data-ttu-id="fbefa-151">Pour une topologie partielle, les nœuds sources de la topologie sont connectés directement aux nœuds de sortie, sans spécifier de transformations intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="fbefa-151">For a partial topology, the topology source nodes are connected directly to the output nodes, without specifying any intermediate transforms.</span></span> <span data-ttu-id="fbefa-152">La session multimédia utilise l’objet de chargeur topologique pour résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="fbefa-152">The Media Session uses the topology loader object to resolve the topology.</span></span> <span data-ttu-id="fbefa-153">Une fois la topologie résolue, les décodeurs requis et les autres nœuds de transformation sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="fbefa-153">After a topology is resolved, the required decoders and other transform nodes are added.</span></span> <span data-ttu-id="fbefa-154">La source de Sequencer peut également contenir des topologies complètes.</span><span class="sxs-lookup"><span data-stu-id="fbefa-154">The sequencer source can also contain full topologies.</span></span>

<span data-ttu-id="fbefa-155">Pour créer l’objet de topologie, utilisez la fonction [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) , puis utilisez l’interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) pour créer des nœuds de flux.</span><span class="sxs-lookup"><span data-stu-id="fbefa-155">To create the topology object, use the [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) function and then use the [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface to create stream nodes.</span></span>

<span data-ttu-id="fbefa-156">Pour obtenir des instructions complètes sur l’utilisation de ces éléments de programmation pour créer des topologies, consultez [création de topologies de lecture](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-156">For complete instructions on using these programming elements to create topologies, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="fbefa-157">Une application peut lire une partie sélectionnée de la source Native en configurant le nœud source.</span><span class="sxs-lookup"><span data-stu-id="fbefa-157">An application can play a selected portion of the native source by configuring the source node.</span></span> <span data-ttu-id="fbefa-158">Pour ce faire, définissez l’attribut [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) et l’attribut [**\_ \_ MEDIASTOP MF TOPONODE**](mf-toponode-mediastop-attribute.md) sur les nœuds de topologie de **\_ \_ \_ nœud SOURCESTREAM** de topologie MF.</span><span class="sxs-lookup"><span data-stu-id="fbefa-158">To do this, set the [**MF\_TOPONODE\_MEDIASTART**](mf-toponode-mediastart-attribute.md) attribute and the [**MF\_TOPONODE\_MEDIASTOP**](mf-toponode-mediastop-attribute.md) attribute on **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** topology nodes.</span></span> <span data-ttu-id="fbefa-159">Spécifiez l’heure de début du média et l’heure d’arrêt du support par rapport au début de la source Native en tant que types **UINT64** .</span><span class="sxs-lookup"><span data-stu-id="fbefa-159">Specify the media start time and the media stop time relative to the start of the native source as **UINT64** types.</span></span>

## <a name="adding-topologies-to-the-sequencer-source"></a><span data-ttu-id="fbefa-160">Ajout de topologies à la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="fbefa-160">Adding Topologies to the Sequencer Source</span></span>

<span data-ttu-id="fbefa-161">Ensuite, ajoutez à la source Sequencer les topologies partielles que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="fbefa-161">Next, add to the sequencer source the partial topologies that you created.</span></span> <span data-ttu-id="fbefa-162">Chaque élément Sequence, appelé *segment*, est associé à un identificateur **MFSequencerElementId** .</span><span class="sxs-lookup"><span data-stu-id="fbefa-162">Each sequence element, called a *segment*, is assigned an **MFSequencerElementId** identifier.</span></span> <span data-ttu-id="fbefa-163">Pour plus d’informations sur la façon dont la source Sequencer gère les topologies, consultez [à propos de la source de Sequencer](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-163">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="fbefa-164">Une fois que toutes les topologies ont été ajoutées à la source de Sequencer, l’application doit marquer le dernier segment dans la séquence pour terminer la lecture dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="fbefa-164">After all of the topologies are added to the sequencer source, the application must flag the last segment in the sequence to end playback in the pipeline.</span></span> <span data-ttu-id="fbefa-165">Sans cet indicateur, la source de Sequencer attend l’ajout de plus de topologies.</span><span class="sxs-lookup"><span data-stu-id="fbefa-165">Without this flag, the sequencer source expects more topologies to be added.</span></span>

1.  <span data-ttu-id="fbefa-166">Appelez la méthode [**IMFSequencerSource :: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) pour ajouter une topologie spécifique à la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fbefa-166">Call the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method to add a specific topology to the sequencer source.</span></span>

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    <span data-ttu-id="fbefa-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) ajoute la topologie spécifiée à la séquence.</span><span class="sxs-lookup"><span data-stu-id="fbefa-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adds the specified topology to the sequence.</span></span> <span data-ttu-id="fbefa-168">Cette méthode retourne l’identificateur de segment dans le paramètre *pdwId* .</span><span class="sxs-lookup"><span data-stu-id="fbefa-168">This method returns the segment identifier in the *pdwId* parameter.</span></span>

    <span data-ttu-id="fbefa-169">Si la topologie est la dernière de la source Sequencer, transmettez SequencerTopologyFlags \_ Last dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="fbefa-169">If the topology is the last one in the sequencer source, pass SequencerTopologyFlags\_Last in the *dwFlags* parameter.</span></span> <span data-ttu-id="fbefa-170">Cette valeur est définie dans l’énumération [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-170">This value is defined in the [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) enumeration.</span></span>

2.  <span data-ttu-id="fbefa-171">Appelez [**IMFSequencerSource :: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) pour mettre à jour les indicateurs de la topologie associée à l’identificateur de segment dans la liste d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fbefa-171">Call [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) to update the flags for the topology associated with the segment identifier in the input list.</span></span> <span data-ttu-id="fbefa-172">Dans ce cas, l’appel indique que le segment spécifié est le dernier segment du séquenceur.</span><span class="sxs-lookup"><span data-stu-id="fbefa-172">In this case, the call indicates that the specified segment is the last segment in the sequencer.</span></span> <span data-ttu-id="fbefa-173">(Cet appel est facultatif si la dernière topologie est spécifiée dans l’appel [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .)</span><span class="sxs-lookup"><span data-stu-id="fbefa-173">(This call is optional if the last topology is specified in the [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) call.)</span></span>

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

<span data-ttu-id="fbefa-174">L’application peut remplacer la topologie d’un segment par une autre topologie en appelant [**IMFSequencerSource :: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) et en passant la nouvelle topologie dans *pTopology*.</span><span class="sxs-lookup"><span data-stu-id="fbefa-174">The application can replace a segment's topology with another topology by calling the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) and passing the new topology in *pTopology*.</span></span> <span data-ttu-id="fbefa-175">S’il existe de nouvelles sources natives dans la nouvelle topologie, les sources sont ajoutées au cache source.</span><span class="sxs-lookup"><span data-stu-id="fbefa-175">If there are new native sources in the new topology, the sources are added to the source cache.</span></span> <span data-ttu-id="fbefa-176">La liste des prérolls est également actualisée.</span><span class="sxs-lookup"><span data-stu-id="fbefa-176">The preroll list is also refreshed.</span></span>

## <a name="setting-the-first-topology-on-the-media-session"></a><span data-ttu-id="fbefa-177">Définition de la première topologie sur la session multimédia</span><span class="sxs-lookup"><span data-stu-id="fbefa-177">Setting the First Topology on the Media Session</span></span>

<span data-ttu-id="fbefa-178">Ensuite, met en file d’attente la première topologie dans la source de séquence sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="fbefa-178">Next, queue the first topology in the sequence source on the Media Session.</span></span> <span data-ttu-id="fbefa-179">Pour récupérer la première topologie à partir de la source de Sequencer, l’application doit appeler la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-179">To get the first topology from the sequencer source, the application must call the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="fbefa-180">Cette méthode retourne la topologie partielle, qui est résolue par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="fbefa-180">This method returns the partial topology, which is resolved by the Media Session.</span></span>

<span data-ttu-id="fbefa-181">Pour plus d’informations sur les topologies partielles, consultez [à propos des topologies](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-181">For information about partial topologies, see [About Topologies](about-topologies.md).</span></span>

1.  <span data-ttu-id="fbefa-182">Récupérez la source du média natif pour la première topologie de la source de séquence.</span><span class="sxs-lookup"><span data-stu-id="fbefa-182">Retrieve the native media source for the first topology of the sequence source.</span></span>
2.  <span data-ttu-id="fbefa-183">Créez un descripteur de présentation pour la source du média en appelant la méthode [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-183">Create a presentation descriptor for the media source by calling the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>
3.  <span data-ttu-id="fbefa-184">Récupérez la topologie associée pour la présentation en appelant la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-184">Retrieve the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
4.  <span data-ttu-id="fbefa-185">Définissez la première topologie sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="fbefa-185">Set the first topology on the Media Session by Calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

    <span data-ttu-id="fbefa-186">Appelez [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) avec le paramètre *DwSetTopologyFlags* défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="fbefa-186">Call [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the *dwSetTopologyFlags* parameter set to **NULL**.</span></span> <span data-ttu-id="fbefa-187">Cela indique à la session multimédia de démarrer la topologie spécifiée lorsque la topologie actuelle est terminée.</span><span class="sxs-lookup"><span data-stu-id="fbefa-187">This instructs the Media Session to start the specified topology when the current topology has been completed.</span></span> <span data-ttu-id="fbefa-188">Étant donné que dans ce cas, la topologie spécifiée est la première topologie et qu’il n’y a pas de présentation actuelle, la session multimédia démarre immédiatement la nouvelle présentation.</span><span class="sxs-lookup"><span data-stu-id="fbefa-188">Because in this case, the specified topology is the first topology and there is no current presentation, the Media Session starts the new presentation immediately.</span></span>

    <span data-ttu-id="fbefa-189">La valeur **null** indique également que la session multimédia doit résoudre la topologie, car la topologie retournée par le fournisseur de topologie est toujours une topologie partielle.</span><span class="sxs-lookup"><span data-stu-id="fbefa-189">The **NULL** value also indicates that Media Session must resolve the topology because the topology returned by the topology provider is always a partial topology.</span></span>


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



## <a name="queuing-the-next-topology-on-the-media-session"></a><span data-ttu-id="fbefa-190">Mise en file d’attente de la topologie suivante sur la session multimédia</span><span class="sxs-lookup"><span data-stu-id="fbefa-190">Queuing the Next Topology on the Media Session</span></span>

<span data-ttu-id="fbefa-191">Ensuite, l’application doit gérer l’événement [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-191">Next, the application needs to handle the [MENewPresentation](menewpresentation.md) event.</span></span>

<span data-ttu-id="fbefa-192">La source de Sequencer déclenche [MENewPresentation](menewpresentation.md) quand la session multimédia commence à exécuter un segment qui en suit un autre segment.</span><span class="sxs-lookup"><span data-stu-id="fbefa-192">Sequencer source raises [MENewPresentation](menewpresentation.md) when the Media Session starts playing a segment that has another segment following it.</span></span> <span data-ttu-id="fbefa-193">Cet événement informe l’application de la topologie suivante dans la source de séquence en fournissant le descripteur de présentation du segment suivant dans la liste des préroll.</span><span class="sxs-lookup"><span data-stu-id="fbefa-193">This event informs the application about the next topology in the sequence source by providing the presentation descriptor for the next segment in the preroll list.</span></span> <span data-ttu-id="fbefa-194">L’application doit récupérer la topologie associée, en utilisant le fournisseur de topologie, et la faire défiler sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="fbefa-194">The application must retrieve the associated topology, by using the topology provider, and queue it on the Media Session.</span></span> <span data-ttu-id="fbefa-195">La source de Sequencer préroll ensuite cette topologie, ce qui garantit une transition transparente entre les présentations.</span><span class="sxs-lookup"><span data-stu-id="fbefa-195">The sequencer source then prerolls this topology, which ensures a seamless transition between presentations.</span></span>

<span data-ttu-id="fbefa-196">Lorsque l’application recherche sur les segments, elle reçoit plusieurs événements [MENewPresentation](menewpresentation.md) , car la source de Sequencer actualise la liste des préroll et configure la topologie correcte.</span><span class="sxs-lookup"><span data-stu-id="fbefa-196">When the application seeks across segments, the application receives several [MENewPresentation](menewpresentation.md) events as the sequencer source refreshes the preroll list and sets up the correct topology.</span></span> <span data-ttu-id="fbefa-197">L’application doit gérer chaque événement et effectuer la mise en file d’attente de la topologie renvoyée dans les données d’événement, sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="fbefa-197">The application must handle each event and queue the topology returned in the event data, on the Media Session.</span></span> <span data-ttu-id="fbefa-198">Pour plus d’informations sur les segments ignorés, consultez [utilisation de la source de Sequencer](using-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-198">For information about skipping segments, see [Using the Sequencer Source](using-the-sequencer-source.md).</span></span>

<span data-ttu-id="fbefa-199">Pour plus d’informations sur l’obtention des notifications de la source de Sequencer, consultez [événements sources de Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="fbefa-199">For information about getting sequencer source notifications, see [Sequencer Source Events](sequencer-source-events.md).</span></span>

1.  <span data-ttu-id="fbefa-200">Dans le gestionnaire d’événements [MENewPresentation](menewpresentation.md) , récupérez le descripteur de présentation du segment suivant à partir des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="fbefa-200">In the [MENewPresentation](menewpresentation.md) event handler, retrieve the presentation descriptor for the next segment from the event data.</span></span>
2.  <span data-ttu-id="fbefa-201">Obtenir la topologie associée pour la présentation en appelant la méthode [**IMFMediaSourceTopologyProvider :: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-201">Get the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
3.  <span data-ttu-id="fbefa-202">Définissez la topologie sur la session de média en appelant la méthode [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .</span><span class="sxs-lookup"><span data-stu-id="fbefa-202">Set the topology on the Media Session by calling the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>

    <span data-ttu-id="fbefa-203">La session multimédia démarre la nouvelle présentation lorsque la présentation en cours est terminée.</span><span class="sxs-lookup"><span data-stu-id="fbefa-203">The Media Session starts the new presentation when the current presentation has been completed.</span></span>


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a><span data-ttu-id="fbefa-204">Libération de la source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="fbefa-204">Releasing the Sequencer Source</span></span>

<span data-ttu-id="fbefa-205">Enfin, arrêtez la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fbefa-205">Finally, shut down the sequencer source.</span></span> <span data-ttu-id="fbefa-206">Pour ce faire, appelez la méthode [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fbefa-206">To do so, call the [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) method on the sequencer source.</span></span> <span data-ttu-id="fbefa-207">Cet appel arrête toutes les sources de média natives sous-jacentes dans la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fbefa-207">This call shuts down all of the underlying native media sources in the sequencer source.</span></span>

<span data-ttu-id="fbefa-208">Après avoir libéré la source de Sequencer, l’application doit fermer et arrêter la session multimédia en appelant [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) et [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="fbefa-208">After releasing the sequencer source, the application should close and shut down the Media Session by calling [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) and [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in that order.</span></span>

<span data-ttu-id="fbefa-209">Pour éviter les fuites de mémoire, l’application doit libérer des pointeurs vers des interfaces Media Foundation lorsqu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="fbefa-209">To avoid memory leaks, the application must release pointers to Media Foundation interfaces when they are no longer needed.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fbefa-210">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fbefa-210">Next Steps</span></span>

<span data-ttu-id="fbefa-211">Cette procédure pas à pas montre comment créer une playlist de base à l’aide de la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fbefa-211">This walk-through illustrated how to create a basic playlist by using the sequencer source.</span></span> <span data-ttu-id="fbefa-212">Après avoir créé la sélection, vous souhaiterez peut-être ajouter des fonctionnalités avancées telles que le saut de segment, la modification de l’état de lecture et la recherche dans un segment.</span><span class="sxs-lookup"><span data-stu-id="fbefa-212">After creating the playlist, you might want to add advanced features such as segment skipping, changing the playback state, and seeking within a segment.</span></span> <span data-ttu-id="fbefa-213">La liste suivante fournit des liens vers les rubriques connexes :</span><span class="sxs-lookup"><span data-stu-id="fbefa-213">The following list provides links to the related topics:</span></span>

-   <span data-ttu-id="fbefa-214">[Comment contrôler les États de présentation](how-to-control-presentation-states.md): la source de Sequencer s’appuie sur la session multimédia pour fournir un contrôle de transport tel que, lecture, pause et arrêt.</span><span class="sxs-lookup"><span data-stu-id="fbefa-214">[How to Control Presentation States](how-to-control-presentation-states.md): The sequencer source relies on the Media Session to provide transport control such as, Play, Pause, and Stop.</span></span>
-   <span data-ttu-id="fbefa-215">[Comment effectuer un nettoyage](how-to-perform-scrubbing.md) de la vue décrit les étapes requises pour rechercher une position spécifique dans un flux.</span><span class="sxs-lookup"><span data-stu-id="fbefa-215">[How to Perform Scrubbing](how-to-perform-scrubbing.md) describes the steps required to seek to a specific position in a stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbefa-216">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fbefa-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbefa-217">Source de Sequencer</span><span class="sxs-lookup"><span data-stu-id="fbefa-217">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



