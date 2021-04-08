---
description: Création de nœuds de sortie
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Création de nœuds de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4388258c82c12f8473dc07df83ba3b9467eed7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861814"
---
# <a name="creating-output-nodes"></a><span data-ttu-id="54698-103">Création de nœuds de sortie</span><span class="sxs-lookup"><span data-stu-id="54698-103">Creating Output Nodes</span></span>

<span data-ttu-id="54698-104">Un nœud de sortie représente un récepteur de flux sur un récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="54698-104">An output node represents a stream sink on a media sink.</span></span> <span data-ttu-id="54698-105">Il existe deux façons d’initialiser un nœud de sortie :</span><span class="sxs-lookup"><span data-stu-id="54698-105">There are two ways to initialize an output node:</span></span>

-   <span data-ttu-id="54698-106">À partir d’un pointeur vers le récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="54698-106">From a pointer to the stream sink.</span></span>
-   <span data-ttu-id="54698-107">À partir d’un pointeur vers un objet d’activation pour le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="54698-107">From a pointer to an activation object for the media sink.</span></span>

<span data-ttu-id="54698-108">Si vous envisagez de charger la topologie à l’intérieur du chemin d’accès de média protégé (PMP), vous devez utiliser un objet d’activation afin que le récepteur multimédia puisse être créé à l’intérieur du processus protégé.</span><span class="sxs-lookup"><span data-stu-id="54698-108">If you are going to load the topology inside the protected media path (PMP), you must use an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="54698-109">La première approche (à l’aide d’un pointeur vers le récepteur de flux) ne fonctionne pas avec l’PMP.</span><span class="sxs-lookup"><span data-stu-id="54698-109">The first approach (using a pointer to the stream sink) does not work with the PMP.</span></span>

## <a name="creating-an-output-node-from-a-stream-sink"></a><span data-ttu-id="54698-110">Création d’un nœud de sortie à partir d’un récepteur de flux</span><span class="sxs-lookup"><span data-stu-id="54698-110">Creating an Output Node from a Stream Sink</span></span>

<span data-ttu-id="54698-111">Pour créer un nœud de sortie à partir d’un récepteur de flux, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="54698-111">To create an output node from a stream sink, do the following:</span></span>

1.  <span data-ttu-id="54698-112">Créez une instance du récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="54698-112">Create an instance of the media sink.</span></span>
2.  <span data-ttu-id="54698-113">Utilisez l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) du récepteur multimédia pour obtenir un pointeur vers le récepteur de flux souhaité.</span><span class="sxs-lookup"><span data-stu-id="54698-113">Use the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface to get a pointer to the desired stream sink.</span></span> <span data-ttu-id="54698-114">(L’interface **IMFMediaSink** possède plusieurs méthodes qui retournent des pointeurs vers un récepteur de flux.)</span><span class="sxs-lookup"><span data-stu-id="54698-114">(The **IMFMediaSink** interface has several methods that return pointers to a stream sink.)</span></span>
3.  <span data-ttu-id="54698-115">Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ sortie \_ de topologie MF** pour créer le nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="54698-115">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
4.  <span data-ttu-id="54698-116">Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez un pointeur vers l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) du récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="54698-116">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in a pointer to the stream sink's [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span>
5.  <span data-ttu-id="54698-117">Affectez la valeur **false** (facultatif mais recommandé) à l’attribut [**TOPONODE de l’option MF \_ sur la \_ \_ \_ suppression**](mf-toponode-noshutdown-on-remove-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="54698-117">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **FALSE** (optional but recommended).</span></span>
6.  <span data-ttu-id="54698-118">Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.</span><span class="sxs-lookup"><span data-stu-id="54698-118">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="54698-119">L’exemple suivant crée et initialise un nœud de sortie à partir d’un récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="54698-119">The following example creates and initializes an output node from a stream sink.</span></span>


```C++
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFStreamSink *pStreamSink, // Stream sink.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    IMFTopologyNode *pNode = NULL;
    HRESULT hr = S_OK;
    
    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pStreamSink);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, TRUE);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    if (pNode)
    {
        pNode->Release();
    }
    return hr;
}
```



<span data-ttu-id="54698-120">Lorsque l’application arrête la session multimédia, la session multimédia arrête automatiquement le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="54698-120">When the application shuts down the Media Session, the Media Session automatically shuts down the media sink.</span></span> <span data-ttu-id="54698-121">Par conséquent, vous ne pouvez pas réutiliser le récepteur multimédia avec une autre instance de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="54698-121">Therefore, you cannot re-use the media sink with another instance of the Media Session.</span></span>

## <a name="creating-an-output-node-from-an-activation-object"></a><span data-ttu-id="54698-122">Création d’un nœud de sortie à partir d’un objet d’activation</span><span class="sxs-lookup"><span data-stu-id="54698-122">Creating an Output Node from an Activation Object</span></span>

<span data-ttu-id="54698-123">Tout récepteur multimédia approuvé doit fournir un objet d’activation, afin que le récepteur multimédia puisse être créé à l’intérieur du processus protégé.</span><span class="sxs-lookup"><span data-stu-id="54698-123">Any trusted media sink must provide an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="54698-124">Pour plus d’informations, consultez [objets d’activation](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="54698-124">For more information, see [Activation Objects](activation-objects.md).</span></span> <span data-ttu-id="54698-125">La fonction particulière qui crée l’objet d’activation dépend du récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="54698-125">The particular function that creates the activation object will depend on the media sink.</span></span>

<span data-ttu-id="54698-126">Pour créer un nœud de sortie à partir d’un objet d’activation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="54698-126">To create an output node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="54698-127">Créez l’objet d’activation et récupérez un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) de l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="54698-127">Create the activation object and get a pointer to the activation object's [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="54698-128">Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ sortie \_ de topologie MF** pour créer le nœud de sortie.</span><span class="sxs-lookup"><span data-stu-id="54698-128">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
3.  <span data-ttu-id="54698-129">Si vous le souhaitez, définissez l’attribut [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) sur le nœud pour spécifier l’identificateur de flux du récepteur de flux.</span><span class="sxs-lookup"><span data-stu-id="54698-129">Optionally, set the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute on the node to specify the stream identifier of the stream sink.</span></span> <span data-ttu-id="54698-130">Si vous omettez cet attribut, le nœud utilise par défaut le récepteur de flux 0.</span><span class="sxs-lookup"><span data-stu-id="54698-130">If you omit this attribute, the node defaults to using stream sink 0.</span></span>
4.  <span data-ttu-id="54698-131">Affectez la **valeur true** (facultatif mais recommandé) à l’attribut [**TOPONODE de l’option MF \_ sur la \_ \_ \_ suppression**](mf-toponode-noshutdown-on-remove-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="54698-131">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **TRUE** (optional but recommended).</span></span>
5.  <span data-ttu-id="54698-132">Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="54698-132">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
6.  <span data-ttu-id="54698-133">Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.</span><span class="sxs-lookup"><span data-stu-id="54698-133">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="54698-134">L’exemple suivant crée et initialise un nœud de sortie à partir d’un objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="54698-134">The following example creates and initializes an output node from an activation object.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="54698-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54698-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54698-136">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="54698-136">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="54698-137">Création de topologies</span><span class="sxs-lookup"><span data-stu-id="54698-137">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="54698-138">Récepteurs de médias</span><span class="sxs-lookup"><span data-stu-id="54698-138">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="54698-139">Topologies</span><span class="sxs-lookup"><span data-stu-id="54698-139">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



