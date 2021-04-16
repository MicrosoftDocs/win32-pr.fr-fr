---
description: Liaison de nœuds de sortie à des récepteurs multimédias
ms.assetid: d4f93f34-0af1-431f-9333-70ea09691b64
title: Liaison de nœuds de sortie à des récepteurs multimédias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbea075badf74ac9e0e9354d82f4100a6167a0c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530478"
---
# <a name="binding-output-nodes-to-media-sinks"></a><span data-ttu-id="e2436-103">Liaison de nœuds de sortie à des récepteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="e2436-103">Binding Output Nodes to Media Sinks</span></span>

<span data-ttu-id="e2436-104">Cette rubrique explique comment initialiser les nœuds de sortie dans une topologie, si vous utilisez le chargeur de topologie en dehors de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e2436-104">This topic describes how to initialize the output nodes in a topology, if you are using the topology loader outside of the Media Session.</span></span> <span data-ttu-id="e2436-105">Un nœud de sortie contient initialement l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e2436-105">An output node initially contains one of the following:</span></span>

-   <span data-ttu-id="e2436-106">Pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="e2436-106">An [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer.</span></span>
-   <span data-ttu-id="e2436-107">Pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="e2436-107">An [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>

<span data-ttu-id="e2436-108">Dans ce dernier cas, le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) doit être converti en pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) avant que le chargeur de topologie ne résout la topologie.</span><span class="sxs-lookup"><span data-stu-id="e2436-108">In the latter case, the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer must be converted to an [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer before the topology loader resolves the topology.</span></span> <span data-ttu-id="e2436-109">Dans la plupart des scénarios, le processus fonctionne comme suit :</span><span class="sxs-lookup"><span data-stu-id="e2436-109">In most scenarios, the process works as follows:</span></span>

1.  <span data-ttu-id="e2436-110">L’application met en file d’attente une topologie partielle sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="e2436-110">The application queues a partial topology on the Media Session.</span></span>
2.  <span data-ttu-id="e2436-111">Pour tous les nœuds de sortie, la session multimédia convertit les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en pointeurs [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="e2436-111">For all output nodes, the Media Session converts [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers to [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointers.</span></span> <span data-ttu-id="e2436-112">Ce processus est appelé *liaison* du nœud de sortie à un récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e2436-112">This process is called *binding* the output node to a media sink.</span></span>
3.  <span data-ttu-id="e2436-113">La session multimédia envoie la topologie modifiée à la méthode [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .</span><span class="sxs-lookup"><span data-stu-id="e2436-113">The Media Session sends the modified topology to the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="e2436-114">Toutefois, si vous utilisez directement le chargeur de topologie (en dehors du session multimédia), votre application doit lier les nœuds de sortie avant d’appeler [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span><span class="sxs-lookup"><span data-stu-id="e2436-114">However, if you are using the topology loader directly (outside of the media sesssion), your application must bind the output nodes prior to calling [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load).</span></span> <span data-ttu-id="e2436-115">Pour lier un nœud de sortie, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e2436-115">To bind an output node, do the following:</span></span>

1.  <span data-ttu-id="e2436-116">Appelez [**IMFTopologyNode :: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) pour récupérer le pointeur d’objet du nœud.</span><span class="sxs-lookup"><span data-stu-id="e2436-116">Call [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) to get the node's object pointer.</span></span>
2.  <span data-ttu-id="e2436-117">Interrogez le pointeur d’objet pour l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="e2436-117">Query the object pointer for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="e2436-118">Si cet appel a échoué, il n’y a rien d’autre à faire, ignorez les étapes restantes.</span><span class="sxs-lookup"><span data-stu-id="e2436-118">If this call succeeds, there is nothing more to do, so skip the remaining steps.</span></span>
3.  <span data-ttu-id="e2436-119">Si l’étape précédente a échoué, interrogez le pointeur d’objet de l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="e2436-119">If the previous step failed, query the object pointer for the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
4.  <span data-ttu-id="e2436-120">Créez le récepteur multimédia en appelant [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="e2436-120">Create the media sink by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="e2436-121">Spécifiez **IID \_ IMFMediaSink** pour obtenir un pointeur vers l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) du récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e2436-121">Specify **IID\_IMFMediaSink** to get a pointer to the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface.</span></span>
5.  <span data-ttu-id="e2436-122">Interrogez le nœud pour l’attribut [**\_ \_ STREAMID TOPONODE MF**](mf-toponode-streamid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e2436-122">Query the node for the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute.</span></span> <span data-ttu-id="e2436-123">La valeur de cet attribut est l’identificateur du récepteur de flux pour ce nœud.</span><span class="sxs-lookup"><span data-stu-id="e2436-123">The value of this attribute is the identifier of the stream sink for this node.</span></span> <span data-ttu-id="e2436-124">Si l’attribut **MF \_ TOPONODE \_ STREAMID** n’est pas défini, l’identificateur de flux par défaut est zéro.</span><span class="sxs-lookup"><span data-stu-id="e2436-124">If the **MF\_TOPONODE\_STREAMID** attribute is not set, the default stream identifier is zero.</span></span>
6.  <span data-ttu-id="e2436-125">Le récepteur de flux approprié existe peut-être déjà sur le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e2436-125">The appropriate stream sink might already exist on the media sink.</span></span> <span data-ttu-id="e2436-126">Pour vérifier, appelez [**IMFMediaSink :: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) sur le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e2436-126">To check, call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) on the media sink.</span></span> <span data-ttu-id="e2436-127">Si le récepteur de flux existe, la méthode retourne un pointeur vers son interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .</span><span class="sxs-lookup"><span data-stu-id="e2436-127">If the stream sink exists, the method returns a pointer to its [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span> <span data-ttu-id="e2436-128">Si cet appel échoue, essayez d’ajouter un nouveau récepteur de flux en appelant [**IMFMediaSink :: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="e2436-128">If this call fails, try to add a new stream sink by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span> <span data-ttu-id="e2436-129">Si les deux appels échouent, cela signifie que le récepteur multimédia ne prend pas en charge l’identificateur de flux demandé et que ce nœud de topologie n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="e2436-129">If both calls fail, it means the media sink does not support the requested stream identifier, and this topology node is not configured correctly.</span></span> <span data-ttu-id="e2436-130">Retournez un code d’erreur et ignorez l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="e2436-130">Return an error code and skip the next step.</span></span>
7.  <span data-ttu-id="e2436-131">Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), en passant le pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) de l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="e2436-131">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), passing in the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer from the previous step.</span></span> <span data-ttu-id="e2436-132">Cet appel remplace le pointeur d’objet du nœud, afin que le nœud contienne un pointeur vers le récepteur de flux, au lieu d’un pointeur vers l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="e2436-132">This call replaces the node's object pointer, so that the node contains a pointer to the stream sink, instead of a pointer to the activation object.</span></span>

<span data-ttu-id="e2436-133">Le code suivant montre comment lier un nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="e2436-133">The following code shows how to bind an output node.</span></span>


```C++
// BindOutputNode
// Sets the IMFStreamSink pointer on an output node.

HRESULT BindOutputNode(IMFTopologyNode *pNode)
{
    IUnknown *pNodeObject = NULL;
    IMFActivate *pActivate = NULL;
    IMFStreamSink *pStream = NULL;
    IMFMediaSink *pSink = NULL;

    // Get the node's object pointer.
    HRESULT hr = pNode->GetObject(&pNodeObject);
    if (FAILED(hr))
    {
        return hr;
    }

    // The object pointer should be one of the following:
    // 1. An activation object for the media sink.
    // 2. The stream sink.

    // If it's #2, then we're already done.

    // First, check if it's an activation object.
    hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

    if (SUCCEEDED(hr))
    {
        DWORD dwStreamID = 0;

        // The object pointer is an activation object. 
        
        // Try to create the media sink.
        hr = pActivate->ActivateObject(IID_PPV_ARGS(&pSink));

        // Look up the stream ID. (Default to zero.)

        if (SUCCEEDED(hr))
        {
           dwStreamID = MFGetAttributeUINT32(pNode, MF_TOPONODE_STREAMID, 0);
        }

        // Now try to get or create the stream sink.

        // Check if the media sink already has a stream sink with the requested ID.

        if (SUCCEEDED(hr))
        {
            hr = pSink->GetStreamSinkById(dwStreamID, &pStream);
            if (FAILED(hr))
            {
                // Try to add a new stream sink.
                hr = pSink->AddStreamSink(dwStreamID, NULL, &pStream);
            }
        }

        // Replace the node's object pointer with the stream sink. 
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pStream);
        }
    }
    else
    {
        // Not an activation object. Is it a stream sink?
        hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pStream));
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pActivate);
    SafeRelease(&pStream);
    SafeRelease(&pSink);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="e2436-134">Cet exemple utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="e2436-134">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="e2436-135">L’exemple suivant montre comment lier tous les nœuds de sortie dans une topologie.</span><span class="sxs-lookup"><span data-stu-id="e2436-135">The next example shows how to bind all of the output nodes in a topology.</span></span> <span data-ttu-id="e2436-136">Cet exemple utilise la méthode [**IMFTopology :: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) pour obtenir une collection de nœuds de sortie à partir de la topologie.</span><span class="sxs-lookup"><span data-stu-id="e2436-136">This example uses the [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) method to get a collection of output nodes from the topology.</span></span> <span data-ttu-id="e2436-137">Elle appelle ensuite la fonction illustrée dans l’exemple précédent sur chacun de ces nœuds à son tour.</span><span class="sxs-lookup"><span data-stu-id="e2436-137">Then it calls the function shown in the previous example on each of those nodes in turn.</span></span>


```C++
// BindOutputNodes
// Sets the IMFStreamSink pointers on all of the output nodes in a topology.

HRESULT BindOutputNodes(IMFTopology *pTopology)
{
    DWORD cNodes = 0;

    IMFCollection *pCol = NULL;
    IUnknown *pUnk = NULL;
    IMFTopologyNode *pNode = NULL;

    // Get the collection of output nodes. 
    HRESULT hr = pTopology->GetOutputNodeCollection(&pCol);
    
    // Enumerate all of the nodes in the collection.
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            hr = pCol->GetElement(i, &pUnk);

            if (FAILED(hr)) { break; }

            hr = pUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);

            if (FAILED(hr)) { break; }

            // Bind this node.
            hr = BindOutputNode(pNode);

            if (FAILED(hr)) { break; }
        }
    }

    SafeRelease(&pCol);
    SafeRelease(&pUnk);
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e2436-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2436-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2436-139">Génération de topologie avancée</span><span class="sxs-lookup"><span data-stu-id="e2436-139">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> <dt>

[<span data-ttu-id="e2436-140">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="e2436-140">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="e2436-141">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="e2436-141">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



