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
# <a name="creating-source-nodes"></a>Création de nœuds sources

Un nœud source représente un flux d’une source de média. Le nœud source doit contenir des pointeurs vers la source du média, le descripteur de présentation et le descripteur de flux.

Pour ajouter un nœud source à une topologie, procédez comme suit :

1.  Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ \_ \_ nœud SOURCESTREAM de topologie MF** pour créer le nœud source.
2.  Définissez l’attribut de la [**\_ \_ source TOPONODE MF**](mf-toponode-source-attribute.md) sur le nœud, avec un pointeur vers la source du média.
3.  Définissez l’attribut de [**\_ \_ \_ descripteur de présentation TOPONODE MF**](mf-toponode-presentation-descriptor-attribute.md) sur le nœud, avec un pointeur vers le descripteur de présentation de la source du média.
4.  Définissez l’attribut de [**\_ \_ \_ descripteur de flux TOPONODE MF**](mf-toponode-stream-descriptor-attribute.md) sur le nœud, avec un pointeur vers le descripteur de flux du flux.
5.  Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.

L’exemple suivant crée et initialise un nœud source.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de topologies](creating-topologies.md)
</dt> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[Topologies](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



