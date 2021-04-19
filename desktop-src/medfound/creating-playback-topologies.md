---
description: Cette rubrique explique comment créer une topologie pour la lecture audio ou vidéo.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Création de topologies de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514368"
---
# <a name="creating-playback-topologies"></a><span data-ttu-id="be6d5-103">Création de topologies de lecture</span><span class="sxs-lookup"><span data-stu-id="be6d5-103">Creating Playback Topologies</span></span>

<span data-ttu-id="be6d5-104">Cette rubrique explique comment créer une topologie pour la lecture audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="be6d5-104">This topic describes how to create a topology for audio or video playback.</span></span> <span data-ttu-id="be6d5-105">Pour la lecture de base, vous pouvez créer une topologie partielle, dans laquelle les nœuds sources sont connectés directement aux nœuds de sortie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-105">For basic playback, you can create a partial topology, in which the source nodes are connected directly to the output nodes.</span></span> <span data-ttu-id="be6d5-106">Vous n’avez pas besoin d’insérer de nœuds pour les transformations intermédiaires, telles que les décodeurs ou les convertisseurs de couleurs.</span><span class="sxs-lookup"><span data-stu-id="be6d5-106">You do not need to insert any nodes for the intermediate transforms, such as decoders or color converters.</span></span> <span data-ttu-id="be6d5-107">La session multimédia utilise le chargeur de topologie pour résoudre la topologie, et le chargeur de topologie insère les transformations qui sont requises.</span><span class="sxs-lookup"><span data-stu-id="be6d5-107">The Media Session will use the topology loader to resolve the topology, and the topology loader will insert the transforms that are required.</span></span>

-   [<span data-ttu-id="be6d5-108">Création de la topologie</span><span class="sxs-lookup"><span data-stu-id="be6d5-108">Creating the Topology</span></span>](#creating-the-topology)
-   [<span data-ttu-id="be6d5-109">Connexion de flux à des récepteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="be6d5-109">Connecting Streams to Media Sinks</span></span>](#connecting-streams-to-media-sinks)
-   [<span data-ttu-id="be6d5-110">Création du récepteur multimédia</span><span class="sxs-lookup"><span data-stu-id="be6d5-110">Creating the Media Sink</span></span>](#creating-the-media-sink)
-   [<span data-ttu-id="be6d5-111">Next Steps</span><span class="sxs-lookup"><span data-stu-id="be6d5-111">Next Steps</span></span>](#next-steps)
-   [<span data-ttu-id="be6d5-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be6d5-112">Related topics</span></span>](#related-topics)

## <a name="creating-the-topology"></a><span data-ttu-id="be6d5-113">Création de la topologie</span><span class="sxs-lookup"><span data-stu-id="be6d5-113">Creating the Topology</span></span>

<span data-ttu-id="be6d5-114">Voici les étapes générales pour créer une topologie de lecture partielle à partir d’une source de média :</span><span class="sxs-lookup"><span data-stu-id="be6d5-114">Here are the overall steps for creating a partial playback topology from a media source:</span></span>

1.  <span data-ttu-id="be6d5-115">Créez la source du média.</span><span class="sxs-lookup"><span data-stu-id="be6d5-115">Create the media source.</span></span> <span data-ttu-id="be6d5-116">Dans la plupart des cas, vous utiliserez le programme de résolution source pour créer la source du média.</span><span class="sxs-lookup"><span data-stu-id="be6d5-116">In most cases, you will use the source resolver to create the media source.</span></span> <span data-ttu-id="be6d5-117">Pour plus d’informations, consultez la page programme de [résolution source](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="be6d5-117">For more information, see [Source Resolver](source-resolver.md).</span></span>
2.  <span data-ttu-id="be6d5-118">Obtient le descripteur de présentation de la source du média.</span><span class="sxs-lookup"><span data-stu-id="be6d5-118">Get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="be6d5-119">Créez une topologie vide.</span><span class="sxs-lookup"><span data-stu-id="be6d5-119">Create an empty topology.</span></span>
4.  <span data-ttu-id="be6d5-120">Utilisez le descripteur de présentation pour énumérer les descripteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-120">Use the presentation descriptor to enumerate the stream descriptors.</span></span> <span data-ttu-id="be6d5-121">Pour chaque descripteur de flux :</span><span class="sxs-lookup"><span data-stu-id="be6d5-121">For each stream descriptor:</span></span>
    1.  <span data-ttu-id="be6d5-122">Obtient le type de média principal du flux, tel que l’audio ou la vidéo.</span><span class="sxs-lookup"><span data-stu-id="be6d5-122">Get the stream's major media type, such as audio or video.</span></span>
    2.  <span data-ttu-id="be6d5-123">Vérifiez si le flux est actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="be6d5-123">Check if the stream is currently selected.</span></span> <span data-ttu-id="be6d5-124">(Si vous le souhaitez, vous pouvez sélectionner ou désélectionner un flux, en fonction du type de média.)</span><span class="sxs-lookup"><span data-stu-id="be6d5-124">(Optionally, you can select or deselect a stream, based on the media type.)</span></span>
    3.  <span data-ttu-id="be6d5-125">Si le flux est sélectionné, créez un objet d’activation pour le récepteur multimédia, en fonction du type de média du flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-125">If the stream is selected, create an activation object for the media sink, based on the stream's media type.</span></span>
    4.  <span data-ttu-id="be6d5-126">Ajoutez un nœud source pour le flux et un nœud de sortie pour le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="be6d5-126">Add a source node for the stream and an output node for the media sink.</span></span>
    5.  <span data-ttu-id="be6d5-127">Connectez le nœud source au nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-127">Connect the source node to the output node.</span></span>

<span data-ttu-id="be6d5-128">Pour faciliter ce processus, l’exemple de code de cette rubrique est organisé en plusieurs fonctions.</span><span class="sxs-lookup"><span data-stu-id="be6d5-128">To make this process easier to follow, the example code in this topic is organized into several functions.</span></span> <span data-ttu-id="be6d5-129">La fonction de niveau supérieur est nommée `CreatePlaybackTopology` .</span><span class="sxs-lookup"><span data-stu-id="be6d5-129">The top-level function is named `CreatePlaybackTopology`.</span></span> <span data-ttu-id="be6d5-130">Il accepte trois paramètres :</span><span class="sxs-lookup"><span data-stu-id="be6d5-130">It takes three parameters:</span></span>

-   <span data-ttu-id="be6d5-131">Pointeur vers une interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="be6d5-131">A pointer to a [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="be6d5-132">Pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="be6d5-132">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span> <span data-ttu-id="be6d5-133">Pour ce faire, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="be6d5-133">Get this pointer by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="be6d5-134">Pour les sources avec plusieurs présentations, les descripteurs de présentation pour les présentations suivantes sont fournis dans l’événement [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="be6d5-134">For sources with multiple presentations, the presentation descriptors for subsequent presentations are delivered in the [MENewPresentation](menewpresentation.md) event.</span></span>
-   <span data-ttu-id="be6d5-135">Handle d’une fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="be6d5-135">A handle to an application window.</span></span> <span data-ttu-id="be6d5-136">Si la source a un flux vidéo, la vidéo s’affiche dans cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="be6d5-136">If the source has a video stream, the video will be displayed in this window.</span></span>

<span data-ttu-id="be6d5-137">La fonction retourne un pointeur vers une topologie de lecture partielle dans le paramètre *ppTopology* .</span><span class="sxs-lookup"><span data-stu-id="be6d5-137">The function returns a pointer to a partial playback topology in the *ppTopology* parameter.</span></span>


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="be6d5-138">Cette fonction effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="be6d5-138">This function performs the following steps:</span></span>

1.  <span data-ttu-id="be6d5-139">Appelez [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) pour créer la topologie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-139">Call [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) to create the topology.</span></span> <span data-ttu-id="be6d5-140">Au départ, la topologie ne contient aucun nœud.</span><span class="sxs-lookup"><span data-stu-id="be6d5-140">Initially, the topology does not contain any nodes.</span></span>
2.  <span data-ttu-id="be6d5-141">Appelez [**IMFPresentationDescriptor :: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) pour connaître le nombre de flux dans la présentation.</span><span class="sxs-lookup"><span data-stu-id="be6d5-141">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the presentation.</span></span>
3.  <span data-ttu-id="be6d5-142">Pour chaque flux, appelez la fonction définie par l’application `AddBranchToPartialTopology` dans une branche de la topologie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-142">For each stream, call the application-defined `AddBranchToPartialTopology` function to a branch in the topology.</span></span> <span data-ttu-id="be6d5-143">Cette fonction est présentée dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="be6d5-143">This function is shown in the next section.</span></span>

## <a name="connecting-streams-to-media-sinks"></a><span data-ttu-id="be6d5-144">Connexion de flux à des récepteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="be6d5-144">Connecting Streams to Media Sinks</span></span>

<span data-ttu-id="be6d5-145">Pour chaque flux sélectionné, ajoutez un nœud source et un nœud de sortie, puis connectez les deux nœuds.</span><span class="sxs-lookup"><span data-stu-id="be6d5-145">For each selected stream, add a source node and an output node, then connect the two nodes.</span></span> <span data-ttu-id="be6d5-146">Le nœud source représente le flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-146">The source node represents the stream.</span></span> <span data-ttu-id="be6d5-147">Le nœud de sortie représente soit le [convertisseur de vidéo amélioré](enhanced-video-renderer.md) (EVR), soit le [convertisseur audio de streaming](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="be6d5-147">The output node represents either the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) or the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

<span data-ttu-id="be6d5-148">La `AddBranchToPartialTopology` fonction, illustrée dans l’exemple suivant, accepte les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="be6d5-148">The `AddBranchToPartialTopology` function, shown in the next example, takes the following parameters:</span></span>

-   <span data-ttu-id="be6d5-149">Pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-149">A pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span>
-   <span data-ttu-id="be6d5-150">Pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média.</span><span class="sxs-lookup"><span data-stu-id="be6d5-150">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="be6d5-151">Pointeur vers l’interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) du descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="be6d5-151">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span>
-   <span data-ttu-id="be6d5-152">Index de base zéro du flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-152">The zero-based index of the stream.</span></span>
-   <span data-ttu-id="be6d5-153">Handle de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="be6d5-153">A handle to the video window.</span></span> <span data-ttu-id="be6d5-154">Ce descripteur est utilisé uniquement pour le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="be6d5-154">This handle is used only for the video stream.</span></span>


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



<span data-ttu-id="be6d5-155">La fonction effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="be6d5-155">The function does the following:</span></span>

1.  <span data-ttu-id="be6d5-156">Appelle [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) et passe l’index de flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-156">Calls [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and passes in the stream index.</span></span> <span data-ttu-id="be6d5-157">Cette méthode retourne un pointeur vers le descripteur de flux pour ce flux, ainsi qu’une valeur booléenne indiquant si le flux est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="be6d5-157">This method returns a pointer to the stream descriptor for that stream, along with a Boolean value indicating whether the stream is selected.</span></span>
2.  <span data-ttu-id="be6d5-158">Si le flux n’est pas sélectionné, la fonction se termine et retourne S \_ OK, car l’application n’a pas besoin de créer une branche de topologie pour un flux, sauf si elle est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="be6d5-158">If the stream is not selected, the function exits and returns S\_OK, because the application does not need to create a topology branch for a stream unless it is selected.</span></span>
3.  <span data-ttu-id="be6d5-159">Si le flux est sélectionné, la fonction termine la branche de topologie comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6d5-159">If the stream is selected, the function completes the topology branch as follows:</span></span>
    1.  <span data-ttu-id="be6d5-160">Crée un objet d’activation pour le récepteur, en appelant la fonction CreateMediaSinkActivate définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="be6d5-160">Creates an activation object for the sink, by calling the application-defined CreateMediaSinkActivate function.</span></span> <span data-ttu-id="be6d5-161">Cette fonction est présentée dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="be6d5-161">This function is shown in the next section.</span></span>
    2.  <span data-ttu-id="be6d5-162">Ajoute un nœud source à la topologie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-162">Adds a source node to the topology.</span></span> <span data-ttu-id="be6d5-163">Le code pour cette étape est présenté dans la rubrique [création de nœuds sources](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="be6d5-163">Code for this step is shown in the topic [Creating Source Nodes](creating-source-nodes.md).</span></span>
    3.  <span data-ttu-id="be6d5-164">Ajoute un nœud de sortie à la topologie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-164">Adds an output node to the topology.</span></span> <span data-ttu-id="be6d5-165">Le code pour cette étape est présenté dans la rubrique [création de nœuds de sortie](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="be6d5-165">Code for this step is shown in the topic [Creating Output Nodes](creating-output-nodes.md).</span></span>
    4.  <span data-ttu-id="be6d5-166">Connecte les deux nœuds en appelant [**IMFTopologyNode :: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) sur le nœud source.</span><span class="sxs-lookup"><span data-stu-id="be6d5-166">Connects the two nodes by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the source node.</span></span> <span data-ttu-id="be6d5-167">En connectant les nœuds, l’application indique que le nœud en amont doit fournir des données au nœud en aval.</span><span class="sxs-lookup"><span data-stu-id="be6d5-167">By connecting the nodes, the application indicates that the upstream node should deliver data to the downstream node.</span></span> <span data-ttu-id="be6d5-168">Un nœud source a une sortie et un nœud de sortie a une entrée, donc les deux index de flux sont nuls.</span><span class="sxs-lookup"><span data-stu-id="be6d5-168">A source node has one output, and an output node has one input, so both stream indexes are zero.</span></span>

<span data-ttu-id="be6d5-169">Des applications plus avancées peuvent sélectionner ou désélectionner des flux, au lieu d’utiliser la configuration par défaut de la source.</span><span class="sxs-lookup"><span data-stu-id="be6d5-169">More advanced applications can select or deselect streams, instead of using the source's default configuration.</span></span> <span data-ttu-id="be6d5-170">Une source peut avoir plusieurs flux, et l’une d’elles peut être sélectionnée par défaut.</span><span class="sxs-lookup"><span data-stu-id="be6d5-170">A source could have multiple streams, and any of them might be selected by default.</span></span> <span data-ttu-id="be6d5-171">Le descripteur de présentation de la source du média possède un ensemble de sélections de flux par défaut.</span><span class="sxs-lookup"><span data-stu-id="be6d5-171">The media source's presentation descriptor has a default set of stream selections.</span></span> <span data-ttu-id="be6d5-172">Dans un fichier vidéo simple avec un flux audio et un flux vidéo uniques, la source du média sélectionne généralement les deux flux par défaut.</span><span class="sxs-lookup"><span data-stu-id="be6d5-172">In a simple video file with a single audio stream and video stream, the media source will usually select both streams by default.</span></span> <span data-ttu-id="be6d5-173">Toutefois, un fichier peut avoir plusieurs flux audio pour différentes langues, ou plusieurs flux vidéo encodés à des vitesses de transmission différentes.</span><span class="sxs-lookup"><span data-stu-id="be6d5-173">However, a file might have multiple audio streams for different languages, or multiple video streams encoded at different bit rates.</span></span> <span data-ttu-id="be6d5-174">Dans ce cas, certains flux sont désélectionnés par défaut.</span><span class="sxs-lookup"><span data-stu-id="be6d5-174">In that case, some of the streams will be unselected by default.</span></span> <span data-ttu-id="be6d5-175">L’application peut modifier la sélection en appelant [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) et [**IMFPresentationDescriptor ::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) sur le descripteur de présentation.</span><span class="sxs-lookup"><span data-stu-id="be6d5-175">The application can change the selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) on the presentation descriptor.</span></span>

## <a name="creating-the-media-sink"></a><span data-ttu-id="be6d5-176">Création du récepteur multimédia</span><span class="sxs-lookup"><span data-stu-id="be6d5-176">Creating the Media Sink</span></span>

<span data-ttu-id="be6d5-177">La fonction Next crée un objet d’activation pour le récepteur multimédia EVR ou SAR.</span><span class="sxs-lookup"><span data-stu-id="be6d5-177">The next function creates an activation object for the EVR or SAR media sink.</span></span>


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



<span data-ttu-id="be6d5-178">Cette fonction effectue les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="be6d5-178">This function performs the following steps:</span></span>

1.  <span data-ttu-id="be6d5-179">Appelle [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sur le descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-179">Calls [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span> <span data-ttu-id="be6d5-180">Cette méthode retourne un pointeur d’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="be6d5-180">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface pointer.</span></span>

2.  <span data-ttu-id="be6d5-181">Appelle [**IMFMediaTypeHandler :: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="be6d5-181">Calls [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="be6d5-182">Cette méthode retourne le GUID du type principal pour le flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-182">This method returns the major type GUID for the stream.</span></span>

3.  <span data-ttu-id="be6d5-183">Si le type de flux est audio, la fonction appelle [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) pour créer l’objet d’activation du convertisseur audio.</span><span class="sxs-lookup"><span data-stu-id="be6d5-183">If the stream type is audio, the function calls [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) to create the audio renderer activation object.</span></span> <span data-ttu-id="be6d5-184">Si le type de flux est vidéo, la fonction appelle [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer l’objet d’activation du convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="be6d5-184">If the stream type is video, the function calls [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the video renderer activation object.</span></span> <span data-ttu-id="be6d5-185">Ces deux fonctions retournent un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="be6d5-185">Both of these functions return a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="be6d5-186">Ce pointeur est utilisé pour initialiser le nœud de sortie du récepteur, comme indiqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="be6d5-186">This pointer is used to initialize the output node for the sink, as shown previously.</span></span>

<span data-ttu-id="be6d5-187">Pour tout autre type de flux, cet exemple retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be6d5-187">For any other stream type, this example returns an error code.</span></span> <span data-ttu-id="be6d5-188">Vous pouvez également désélectionner simplement le flux.</span><span class="sxs-lookup"><span data-stu-id="be6d5-188">Alternatively, you could simply deselect the stream.</span></span>

## <a name="next-steps"></a><span data-ttu-id="be6d5-189">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="be6d5-189">Next Steps</span></span>

<span data-ttu-id="be6d5-190">Pour lire un fichier multimédias à la fois, en file d’attente sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="be6d5-190">To play one media file at a time, queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="be6d5-191">La session multimédia utilise le chargeur de topologie pour résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="be6d5-191">The Media Session will use the topology loader to resolve the topology.</span></span> <span data-ttu-id="be6d5-192">Pour obtenir un exemple complet, consultez [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="be6d5-192">For a complete example, see [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="be6d5-193">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be6d5-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be6d5-194">Comment lire des fichiers multimédias non protégés</span><span class="sxs-lookup"><span data-stu-id="be6d5-194">How to Play Unprotected Media Files</span></span>](how-to-play-unprotected-media-files.md)
</dt> <dt>

[<span data-ttu-id="be6d5-195">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="be6d5-195">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="be6d5-196">Topologies</span><span class="sxs-lookup"><span data-stu-id="be6d5-196">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



