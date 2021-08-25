---
description: Création de nœuds de sortie
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Création de nœuds de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af2842458fb360374d34583b15bfbf5005b2f2bbdd8b32332bc6756ca4e8157
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943019"
---
# <a name="creating-output-nodes"></a>Création de nœuds de sortie

Un nœud de sortie représente un récepteur de flux sur un récepteur multimédia. Il existe deux façons d’initialiser un nœud de sortie :

-   À partir d’un pointeur vers le récepteur de flux.
-   À partir d’un pointeur vers un objet d’activation pour le récepteur multimédia.

Si vous envisagez de charger la topologie à l’intérieur du chemin d’accès de média protégé (PMP), vous devez utiliser un objet d’activation afin que le récepteur multimédia puisse être créé à l’intérieur du processus protégé. La première approche (à l’aide d’un pointeur vers le récepteur de flux) ne fonctionne pas avec l’PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Création d’un nœud de sortie à partir d’un récepteur de flux

Pour créer un nœud de sortie à partir d’un récepteur de flux, procédez comme suit :

1.  Créez une instance du récepteur multimédia.
2.  Utilisez l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) du récepteur multimédia pour obtenir un pointeur vers le récepteur de flux souhaité. (L’interface **IMFMediaSink** possède plusieurs méthodes qui retournent des pointeurs vers un récepteur de flux.)
3.  Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ sortie \_ de topologie MF** pour créer le nœud de sortie.
4.  Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez un pointeur vers l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) du récepteur de flux.
5.  Affectez la valeur **false** (facultatif mais recommandé) à l’attribut [**TOPONODE de l’option MF \_ sur la \_ \_ \_ suppression**](mf-toponode-noshutdown-on-remove-attribute.md) .
6.  Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.

L’exemple suivant crée et initialise un nœud de sortie à partir d’un récepteur de flux.


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



Lorsque l’application arrête la session multimédia, la session multimédia arrête automatiquement le récepteur multimédia. Par conséquent, vous ne pouvez pas réutiliser le récepteur multimédia avec une autre instance de la session multimédia.

## <a name="creating-an-output-node-from-an-activation-object"></a>Création d’un nœud de sortie à partir d’un objet d’activation

Tout récepteur multimédia approuvé doit fournir un objet d’activation, afin que le récepteur multimédia puisse être créé à l’intérieur du processus protégé. Pour plus d’informations, consultez [objets d’activation](activation-objects.md). La fonction particulière qui crée l’objet d’activation dépend du récepteur multimédia.

Pour créer un nœud de sortie à partir d’un objet d’activation, procédez comme suit :

1.  Créez l’objet d’activation et récupérez un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) de l’objet d’activation.
2.  Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ sortie \_ de topologie MF** pour créer le nœud de sortie.
3.  Si vous le souhaitez, définissez l’attribut [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) sur le nœud pour spécifier l’identificateur de flux du récepteur de flux. Si vous omettez cet attribut, le nœud utilise par défaut le récepteur de flux 0.
4.  Affectez la **valeur true** (facultatif mais recommandé) à l’attribut [**TOPONODE de l’option MF \_ sur la \_ \_ \_ suppression**](mf-toponode-noshutdown-on-remove-attribute.md) .
5.  Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
6.  Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.

L’exemple suivant crée et initialise un nœud de sortie à partir d’un objet d’activation.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Création de topologies](creating-topologies.md)
</dt> <dt>

[Récepteurs de médias](media-sinks.md)
</dt> <dt>

[Topologies](topologies.md)
</dt> </dl>

 

 



