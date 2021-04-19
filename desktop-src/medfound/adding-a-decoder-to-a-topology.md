---
description: Ajout d’un décodeur à une topologie
ms.assetid: 32c088d5-d9dd-43d3-a63b-219e6a7a36b1
title: Ajout d’un décodeur à une topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506963ee65490365b60788808a4da87c21355247
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538851"
---
# <a name="adding-a-decoder-to-a-topology"></a>Ajout d’un décodeur à une topologie

Cette rubrique explique comment ajouter un décodeur audio ou vidéo à une topologie.

Pour la plupart des applications de lecture, vous pouvez omettre les décodeurs de la topologie partielle que vous envoyez à la session multimédia. La session multimédia utilise le chargeur de topologie pour terminer la topologie, et le chargeur de topologie insère tous les décodeurs nécessaires. Toutefois, si vous souhaitez sélectionner un décodeur particulier, vous pouvez ajouter manuellement un décodeur à la topologie.

Voici les étapes générales pour l’ajout d’un décodeur à une topologie.

1.  Recherchez le CLSID du décodeur.
2.  Ajoutez un nœud pour le décodeur dans la topologie.
3.  Pour un décodeur vidéo, activez l’accélération vidéo DirectX. Cette étape n’est pas requise pour les décodeurs audio.

## <a name="find-the-decoder-clsid"></a>Rechercher le CLSID du décodeur

Si vous souhaitez utiliser un décodeur particulier, vous connaissez peut-être déjà le CLSID du décodeur. Si c’est le cas, vous pouvez ignorer cette étape. Sinon, utilisez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) pour rechercher le CLSID dans le registre. Cette fonction accepte plusieurs critères de recherche comme entrée. Pour rechercher un décodeur, vous devez spécifier uniquement le format d’entrée (type et sous-type principal). Vous pouvez les récupérer à partir du descripteur de flux, comme indiqué dans le code suivant.


```C++
// Returns the MFT decoder based on the major type GUID.

HRESULT GetDecoderCategory(const GUID& majorType, GUID *pCategory)
{
    if (majorType == MFMediaType_Video)
    {
        *pCategory = MFT_CATEGORY_VIDEO_DECODER;
    }
    else if (majorType == MFMediaType_Audio)
    {
        *pCategory = MFT_CATEGORY_AUDIO_DECODER;
    }
    else
    {
        return MF_E_INVALIDMEDIATYPE;
    }
    return S_OK;
}

// Finds a decoder for a stream.
//
// If the stream is not compressed, pCLSID receives the value GUID_NULL.

HRESULT FindDecoderForStream(
    IMFStreamDescriptor *pSD,   // Stream descriptor for the stream.
    CLSID *pCLSID               // Receives the CLSID of the decoder.
    )
{
    BOOL    bIsCompressed = FALSE;
    GUID    guidMajorType = GUID_NULL;
    GUID    guidSubtype = GUID_NULL;
    GUID    guidDecoderCategory = GUID_NULL;

    CLSID *pDecoderCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cDecoderCLSIDs = NULL;   // Size of the array.

    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pMediaType = NULL;

    // Find the media type for the stream.
    HRESULT hr = pSD->GetMediaTypeHandler(&pHandler);

    if (SUCCEEDED(hr))
    {
        hr = pHandler->GetCurrentMediaType(&pMediaType);
    }

    // Get the major type and subtype.
    if (SUCCEEDED(hr))
    {
        hr = pMediaType->GetMajorType(&guidMajorType);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMediaType->GetGUID(MF_MT_SUBTYPE, &guidSubtype);
    }

    // Check whether the stream is compressed.
    if (SUCCEEDED(hr))
    {
        hr = pMediaType->IsCompressedFormat(&bIsCompressed);
    }

#if (WINVER < _WIN32_WINNT_WIN7)

    // Starting in Windows 7, you can connect an uncompressed video source 
    // directly to the EVR. In earlier versions of Media Foundation, this
    // is not supported.

    if (SUCCEEDED(hr))
    {
        if (!bIsCompressed && (guidMajorType == MFMediaType_Video))
        {
            hr = MF_E_INVALIDMEDIATYPE;
        }
    }
#endif

    // If the stream is compressed, find a decoder.
    if (SUCCEEDED(hr))
    {
        if (bIsCompressed)
        {
            // Select the decoder category from the major type (audio/video).
            hr = GetDecoderCategory(guidMajorType, &guidDecoderCategory);

            // Look for a decoder.

            if (SUCCEEDED(hr))
            {
                MFT_REGISTER_TYPE_INFO tinfo;
                tinfo.guidMajorType = guidMajorType;
                tinfo.guidSubtype = guidSubtype;

                hr = MFTEnum(
                        guidDecoderCategory,
                        0,               // Reserved
                        &tinfo,          // Input type to match. (Encoded type.)
                        NULL,            // Output type to match. (Don't care.)
                        NULL,            // Attributes to match. (None.)
                        &pDecoderCLSIDs, // Receives a pointer to an array of CLSIDs.
                        &cDecoderCLSIDs  // Receives the size of the array.
                        );
            }

            // MFTEnum can return zero matches.
            if (SUCCEEDED(hr) && (cDecoderCLSIDs == 0))
            {
                hr = MF_E_TOPO_CODEC_NOT_FOUND;
            }

            // Return the first CLSID in the list to the caller.
            if (SUCCEEDED(hr))
            {
                *pCLSID = pDecoderCLSIDs[0];
            }
        }
        else
        {
            // Uncompressed. A decoder is not required.
            *pCLSID = GUID_NULL;
        }
    }

    SafeRelease(&pHandler);
    SafeRelease(&pMediaType);
    CoTaskMemFree(pDecoderCLSIDs);

    return hr;
}
```



Pour plus d’informations sur les descripteurs de flux, consultez [descripteurs de présentation](presentation-descriptors.md).

La fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) retourne un pointeur vers un tableau de CLSID. L’ordre du tableau retourné est arbitraire. Dans cet exemple, la fonction utilise le premier CLSID dans le tableau. Vous pouvez obtenir plus d’informations sur un décodeur, y compris le nom convivial du décodeur, en appelant [**MFTGetInfo**](/windows/desktop/api/mfapi/nf-mfapi-mftgetinfo). Notez également que **MFTEnum** peut s’effectuer correctement mais retourner un tableau vide. il est donc important de vérifier la taille du tableau, qui est retournée dans le dernier paramètre.

## <a name="add-the-decoder-node-to-the-topology"></a>Ajouter le nœud décodeur à la topologie

Une fois que vous avez le CLSID pour le décodeur, créez un nouveau nœud de transformation en appelant [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Spécifiez le CLSID en définissant l’attribut d' [**\_ \_ \_ ObjectID de transformation TOPONODE MF**](mf-toponode-transform-objectid-attribute.md) sur le nœud. Pour obtenir un exemple de création d’un nœud de transformation, consultez [création de nœuds de transformation](creating-transform-nodes.md). Connectez ensuite le nœud source au nœud décodeur et le nœud décodeur au nœud de sortie en appelant [**IMFTopologyNode :: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput).

L’exemple suivant montre comment créer les nœuds et les connecter. L’exemple est très similaire à l’exemple de fonction nommé `AddBranchToPartialTopology` qui est illustré dans la rubrique [création de topologies de lecture](creating-playback-topologies.md). La seule différence est que cet exemple ajoute le nœud supplémentaire pour le décodeur.


```C++
HRESULT AddBranchToPartialTopologyWithDecoder(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd                  // Window for video playback.
    )
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;
    IMFTopologyNode     *pDecoderNode = NULL;

    BOOL fSelected = FALSE;
    CLSID clsidDecoder = GUID_NULL;

    // Get the stream descriptor.
    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        return hr;
    }

    if (fSelected)
    {
        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);

        // Create the media sink activation object.
        if (SUCCEEDED(hr))
        {
            hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        }

        // Create the output node for the renderer.
        if (SUCCEEDED(hr))
        {
            hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        }

        // Find a decoder.
        if (SUCCEEDED(hr))
        {
            hr = FindDecoderForStream(pSD, &clsidDecoder);
        }

        if (SUCCEEDED(hr))
        {
            if (clsidDecoder == GUID_NULL)
            {
                // No decoder is required. 
                // Connect the source node to the output node.
                hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
            }
            else
            {
                // Add a decoder node.
                hr = AddTransformNode(pTopology, clsidDecoder, &pDecoderNode);

                // Connect the source node to the decoder node.
                if (SUCCEEDED(hr))
                {
                    hr = pSourceNode->ConnectOutput(0, pDecoderNode, 0);
                }

                // Connect the decoder node to the output node.
                if (SUCCEEDED(hr))
                {
                    hr = pDecoderNode->ConnectOutput(0, pOutputNode, 0);
                }
            }
        }

        // Mark this branch as not requiring a decoder.
        if (SUCCEEDED(hr))
        {
            hr = pOutputNode->SetUINT32(
                MF_TOPONODE_CONNECT_METHOD, 
                MF_CONNECT_ALLOW_CONVERTER
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pDecoderNode->SetUINT32(
                MF_TOPONODE_CONNECT_METHOD, 
                MF_CONNECT_ALLOW_CONVERTER
                );
        }

    }
    // else: If not selected, don't add the branch. 

    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pDecoderNode);

    return hr;
}
```



## <a name="enable-video-acceleration"></a>Activer l’accélération vidéo

L’étape suivante de l’ajout d’un décodeur audio ou vidéo à une topologie s’applique uniquement aux décodeurs vidéo. Pour obtenir des performances optimales pour la lecture vidéo, vous devez activer DirectX Video Acceleration (DXVA) si le décodeur vidéo le prend en charge. En général, cette étape est effectuée par le chargeur de topologie, mais si vous ajoutez manuellement le décodeur à la topologie, vous devez effectuer cette étape vous-même.

En guise de condition préalable pour cette étape, tous les nœuds de sortie de la topologie doivent être liés aux récepteurs de médias. Pour plus d’informations, consultez [liaison de nœuds de sortie à des récepteurs multimédias](binding-output-nodes-to-media-sinks.md).

Tout d’abord, recherchez l’objet dans la topologie qui héberge le gestionnaire de périphériques Direct3D. Pour ce faire, récupérez le pointeur d’objet à partir de chaque nœud et interrogez l’objet pour le service [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . En général, le convertisseur vidéo amélioré (EVR) sert ce rôle. Le code suivant illustre une fonction qui recherche le gestionnaire de périphériques :


```C++
// Finds the node in the topology that provides the Direct3D device manager. 

HRESULT FindDeviceManager(
    IMFTopology *pTopology,         // Topology to search.
    IUnknown **ppDeviceManager,     // Receives a pointer to the device manager.
    IMFTopologyNode **ppNode        // Receives a pointer to the node.
    )
{
    HRESULT hr = S_OK;
    WORD cNodes = 0;
    BOOL bFound = FALSE;

    IMFTopologyNode *pNode = NULL;
    IUnknown *pNodeObject = NULL;
    IDirect3DDeviceManager9 *pD3DManager = NULL;

    // Search all of the nodes in the topology.
    
    hr = pTopology->GetNodeCount(&cNodes);

    if (FAILED(hr))
    {
        return hr;
    }

    for (WORD i = 0; i < cNodes; i++)
    {
        // For each of the following calls, failure just means we 
        // did not find the node we're looking for, so keep looking. 

        hr = pTopology->GetNode(i, &pNode);

        // Get the node's object pointer.
        if (SUCCEEDED(hr))
        {
            hr = pNode->GetObject(&pNodeObject);
        }

        // Query the node object for the device manager service.
        if (SUCCEEDED(hr))
        {
            hr = MFGetService(
                pNodeObject, 
                MR_VIDEO_ACCELERATION_SERVICE, 
                IID_PPV_ARGS(&pD3DManager)
                );
        }

        if (SUCCEEDED(hr))
        {
            // Found the right node. Return the pointers to the caller.
            *ppDeviceManager = pD3DManager;
            (*ppDeviceManager)->AddRef();

            *ppNode = pNode;
            (*ppNode)->AddRef();

            bFound = TRUE;
            break;
        }

        SafeRelease(&pNodeObject);
        SafeRelease(&pD3DManager);
        SafeRelease(&pNode);

    } // End of for loop.

    SafeRelease(&pNodeObject);
    SafeRelease(&pD3DManager);
    SafeRelease(&pNode);

    return bFound ? S_OK : E_FAIL;
}
```



Recherchez ensuite le nœud de transformation qui est directement en amont du nœud qui contient le gestionnaire de périphériques Direct3D. Obtient le pointeur [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) à partir de ce nœud de transformation. Le pointeur **IMFTransform** représente une transformation de Media Foundation (MFT). Selon la façon dont le nœud a été créé, vous devrez peut-être créer la MFT en appelant **CoCreateInstance** ou activer la MFT à partir d’un objet d’activation. Le code suivant gère tous les cas :


```C++
// Returns the MFT for a transform node.

HRESULT GetTransformFromNode(
    IMFTopologyNode *pNode, 
    IMFTransform **ppMFT
    )
{
    MF_TOPOLOGY_TYPE type = MF_TOPOLOGY_MAX;

    IUnknown *pNodeObject = NULL;
    IMFTransform *pMFT = NULL;
    IMFActivate *pActivate = NULL;
    IMFAttributes *pAttributes = NULL;

    // Is this a transform node?
    HRESULT hr = pNode->GetNodeType(&type);

    if (FAILED(hr))
    {
        return hr;
    }

    if (type != MF_TOPOLOGY_TRANSFORM_NODE)
    {
        // Wrong node type.
        return E_FAIL;
    }

    // Check whether the node has an object pointer.
    hr = pNode->GetObject(&pNodeObject);

    if (SUCCEEDED(hr))
    {
        // The object pointer should be one of the following:
        // 1. Pointer to an MFT.
        // 2. Pointer to an activation object.

        // Is it an MFT? Query for IMFTransform.
        hr = pNodeObject->QueryInterface(IID_IMFTransform, (void**)&pMFT);
        if (FAILED(hr))
        {
            // It is not an MFT, so it should be an activation object.
            hr = pNodeObject->QueryInterface(IID_PPV_ARGS(&pActivate));

            // Use the activation object to create the MFT.

            if (SUCCEEDED(hr))
            {
                hr = pActivate->ActivateObject(IID_PPV_ARGS(&pMFT));
            }

            // Replace the node's object pointer with the MFT.
            if (SUCCEEDED(hr))
            {
                hr = pNode->SetObject(pMFT);
            }

            // If the activation object has the MF_ACTIVATE_MFT_LOCKED 
            // attribute, transfer this value to the
            // MF_TOPONODE_MFT_LOCKED attribute on the node.
            // However, don't fail if this attribute is not found.
            if (SUCCEEDED(hr))
            {
                BOOL bLocked = MFGetAttributeUINT32(
                    pActivate, MF_ACTIVATE_MFT_LOCKED, FALSE);


                hr = pNode->SetUINT32(MF_TOPONODE_LOCKED, bLocked);
            }
        }
    }
    else
    {
        GUID clsidMFT;

        // The node does not have an object pointer. Look for a CLSID.
        hr = pNode->GetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, &clsidMFT);
       
        // Create the MFT.
        if (SUCCEEDED(hr))
        {
            hr = CoCreateInstance(
                clsidMFT, NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pMFT)
                );
        }

        // If the MFT supports attributes, copy the node attributes to the 
        // MFT attribute store. 
        if (SUCCEEDED(hr))
        {
            if (SUCCEEDED(pMFT->GetAttributes(&pAttributes)))
            {
                // Copy from pNode to pAttributes.
                hr = pNode->CopyAllItems(pAttributes); 
            }
        }

        // Set the object on the node.
        if (SUCCEEDED(hr))
        {
            hr = pNode->SetObject(pMFT);
        }
    }

    // Return the IMFTransform pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    SafeRelease(&pNodeObject);
    SafeRelease(&pMFT);
    SafeRelease(&pActivate);
    SafeRelease(&pAttributes);
    return hr;
}
```



Si la table MFT a l’attribut prenant en charge la fonction [**\_ \_ D3D \_ MF sa**](mf-sa-d3d-aware-attribute.md) avec la valeur **true**, cela signifie que la table MFT prend en charge l’accélération vidéo DirectX. La fonction suivante teste pour cet attribut :


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



Pour activer l’accélération vidéo sur cette table MFT, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de l’ensemble de messages MFT du \_ \_ \_ \_ Gestionnaire D3D. Affectez également la **valeur true** à l’attribut [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md) sur le nœud transformer. Cet attribut indique au pipeline que l’accélération vidéo a été activée. Le code suivant effectue les étapes suivantes :


```C++
// Enables or disables DirectX Video Acceleration in a topology.

HRESULT EnableVideoAcceleration(IMFTopology *pTopology, BOOL bEnable)
{
    IMFTopologyNode *pD3DManagerNode = NULL;
    IMFTopologyNode *pUpstreamNode = NULL;
    IUnknown *pD3DManager = NULL;
    IMFTransform *pMFT = NULL;

    // Look for the node that supports the Direct3D Manager.
    
    HRESULT hr = FindDeviceManager(pTopology, &pD3DManager, &pD3DManagerNode); 
    if (FAILED(hr))
    {
        //  There is no Direct3D device manager in the topology.
        //  This is not a failure case.
        return S_OK;
    }

    DWORD dwOutputIndex = 0;

    // Get the node upstream from the device manager node.
    hr = pD3DManagerNode->GetInput(0, &pUpstreamNode, &dwOutputIndex);

    // Get the MFT from the upstream node.
    if (SUCCEEDED(hr))
    {
        hr = GetTransformFromNode(pUpstreamNode, &pMFT);
    }

    // If the MFT is Direct3D-aware, notify the MFT of the device 
    // manager and mark the topology node as Direct3D-aware.
    if (SUCCEEDED(hr))
    {
        if (IsTransformD3DAware(pMFT))
        {
            ULONG_PTR ptr = bEnable ? (ULONG_PTR)pD3DManager : NULL;

            hr = pMFT->ProcessMessage(MFT_MESSAGE_SET_D3D_MANAGER, ptr);

            // Mark the node.
            if (SUCCEEDED(hr))
            {
                hr = pUpstreamNode->SetUINT32(MF_TOPONODE_D3DAWARE, bEnable);
            }
        }
    }

    SafeRelease(&pD3DManagerNode);
    SafeRelease(&pUpstreamNode);
    SafeRelease(&pD3DManager);
    SafeRelease(&pMFT);
    return hr;
}
```



Pour plus d’informations sur DXVA dans Media Foundation, consultez [DirectX Video Acceleration 2,0](directx-video-acceleration-2-0.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération de topologie avancée](advanced-topology-building.md)
</dt> </dl>

 

 



