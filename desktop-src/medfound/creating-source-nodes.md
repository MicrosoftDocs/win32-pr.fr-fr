---
description: Création de nœuds sources
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Création de nœuds sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522660"
---
# <a name="creating-source-nodes"></a><span data-ttu-id="2c85f-103">Création de nœuds sources</span><span class="sxs-lookup"><span data-stu-id="2c85f-103">Creating Source Nodes</span></span>

<span data-ttu-id="2c85f-104">Un nœud source représente un flux d’une source de média.</span><span class="sxs-lookup"><span data-stu-id="2c85f-104">A source node represents one stream from a media source.</span></span> <span data-ttu-id="2c85f-105">Le nœud source doit contenir des pointeurs vers la source du média, le descripteur de présentation et le descripteur de flux.</span><span class="sxs-lookup"><span data-stu-id="2c85f-105">The source node must contain pointers to the media source, the presentation descriptor, and the stream descriptor.</span></span>

<span data-ttu-id="2c85f-106">Pour ajouter un nœud source à une topologie, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2c85f-106">To add a source node to a topology, do the following:</span></span>

1.  <span data-ttu-id="2c85f-107">Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ \_ \_ nœud SOURCESTREAM de topologie MF** pour créer le nœud source.</span><span class="sxs-lookup"><span data-stu-id="2c85f-107">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** flag to create the source node.</span></span>
2.  <span data-ttu-id="2c85f-108">Définissez l’attribut de la [**\_ \_ source TOPONODE MF**](mf-toponode-source-attribute.md) sur le nœud, avec un pointeur vers la source du média.</span><span class="sxs-lookup"><span data-stu-id="2c85f-108">Set the [**MF\_TOPONODE\_SOURCE**](mf-toponode-source-attribute.md) attribute on the node, with a pointer to the media source.</span></span>
3.  <span data-ttu-id="2c85f-109">Définissez l’attribut de [**\_ \_ \_ descripteur de présentation TOPONODE MF**](mf-toponode-presentation-descriptor-attribute.md) sur le nœud, avec un pointeur vers le descripteur de présentation de la source du média.</span><span class="sxs-lookup"><span data-stu-id="2c85f-109">Set the [**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) attribute on the node, with a pointer to the presentation descriptor of the media source.</span></span>
4.  <span data-ttu-id="2c85f-110">Définissez l’attribut de [**\_ \_ \_ descripteur de flux TOPONODE MF**](mf-toponode-stream-descriptor-attribute.md) sur le nœud, avec un pointeur vers le descripteur de flux du flux.</span><span class="sxs-lookup"><span data-stu-id="2c85f-110">Set the [**MF\_TOPONODE\_STREAM\_DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) attribute on the node, with a pointer to the stream descriptor for the stream.</span></span>
5.  <span data-ttu-id="2c85f-111">Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.</span><span class="sxs-lookup"><span data-stu-id="2c85f-111">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="2c85f-112">L’exemple suivant crée et initialise un nœud source.</span><span class="sxs-lookup"><span data-stu-id="2c85f-112">The following example creates and initializes a source node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
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



## <a name="related-topics"></a><span data-ttu-id="2c85f-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c85f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c85f-114">Création de topologies</span><span class="sxs-lookup"><span data-stu-id="2c85f-114">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="2c85f-115">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="2c85f-115">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="2c85f-116">Topologies</span><span class="sxs-lookup"><span data-stu-id="2c85f-116">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="2c85f-117">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="2c85f-117">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



