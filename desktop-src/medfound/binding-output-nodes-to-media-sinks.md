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
# <a name="binding-output-nodes-to-media-sinks"></a>Liaison de nœuds de sortie à des récepteurs multimédias

Cette rubrique explique comment initialiser les nœuds de sortie dans une topologie, si vous utilisez le chargeur de topologie en dehors de la session multimédia. Un nœud de sortie contient initialement l’un des éléments suivants :

-   Pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) .
-   Pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

Dans ce dernier cas, le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) doit être converti en pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) avant que le chargeur de topologie ne résout la topologie. Dans la plupart des scénarios, le processus fonctionne comme suit :

1.  L’application met en file d’attente une topologie partielle sur la session multimédia.
2.  Pour tous les nœuds de sortie, la session multimédia convertit les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) en pointeurs [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Ce processus est appelé *liaison* du nœud de sortie à un récepteur multimédia.
3.  La session multimédia envoie la topologie modifiée à la méthode [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

Toutefois, si vous utilisez directement le chargeur de topologie (en dehors du session multimédia), votre application doit lier les nœuds de sortie avant d’appeler [**IMFTopoLoader :: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load). Pour lier un nœud de sortie, procédez comme suit :

1.  Appelez [**IMFTopologyNode :: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject) pour récupérer le pointeur d’objet du nœud.
2.  Interrogez le pointeur d’objet pour l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Si cet appel a échoué, il n’y a rien d’autre à faire, ignorez les étapes restantes.
3.  Si l’étape précédente a échoué, interrogez le pointeur d’objet de l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Créez le récepteur multimédia en appelant [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). Spécifiez **IID \_ IMFMediaSink** pour obtenir un pointeur vers l’interface [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) du récepteur multimédia.
5.  Interrogez le nœud pour l’attribut [**\_ \_ STREAMID TOPONODE MF**](mf-toponode-streamid-attribute.md) . La valeur de cet attribut est l’identificateur du récepteur de flux pour ce nœud. Si l’attribut **MF \_ TOPONODE \_ STREAMID** n’est pas défini, l’identificateur de flux par défaut est zéro.
6.  Le récepteur de flux approprié existe peut-être déjà sur le récepteur multimédia. Pour vérifier, appelez [**IMFMediaSink :: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) sur le récepteur multimédia. Si le récepteur de flux existe, la méthode retourne un pointeur vers son interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Si cet appel échoue, essayez d’ajouter un nouveau récepteur de flux en appelant [**IMFMediaSink :: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Si les deux appels échouent, cela signifie que le récepteur multimédia ne prend pas en charge l’identificateur de flux demandé et que ce nœud de topologie n’est pas configuré correctement. Retournez un code d’erreur et ignorez l’étape suivante.
7.  Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject), en passant le pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) de l’étape précédente. Cet appel remplace le pointeur d’objet du nœud, afin que le nœud contienne un pointeur vers le récepteur de flux, au lieu d’un pointeur vers l’objet d’activation.

Le code suivant montre comment lier un nœud de sortie.


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
> Cet exemple utilise la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.

 

L’exemple suivant montre comment lier tous les nœuds de sortie dans une topologie. Cet exemple utilise la méthode [**IMFTopology :: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) pour obtenir une collection de nœuds de sortie à partir de la topologie. Elle appelle ensuite la fonction illustrée dans l’exemple précédent sur chacun de ces nœuds à son tour.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération de topologie avancée](advanced-topology-building.md)
</dt> <dt>

[Récepteurs de médias](media-sinks.md)
</dt> <dt>

[**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)
</dt> </dl>

 

 



