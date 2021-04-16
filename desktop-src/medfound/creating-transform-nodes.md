---
description: Création de nœuds de transformation
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Création de nœuds de transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524612"
---
# <a name="creating-transform-nodes"></a>Création de nœuds de transformation

Un nœud de transformation représente une Media Foundation transformation (MFT), telle qu’un décodeur ou un encodeur. Il existe plusieurs façons d’initialiser un nœud transformer :

-   À partir d’un pointeur vers la table MFT.
-   À partir d’un CLSID pour la table MFT.
-   À partir d’un pointeur vers un objet d’activation pour la table MFT.

Si vous envisagez de charger la topologie à l’intérieur du chemin d’accès de média protégé (PMP), vous devez utiliser le CLSID ou un objet d’activation, afin que la table MFT puisse être créée à l’intérieur du processus protégé. La première approche (à l’aide d’un pointeur vers la table MFT) ne fonctionne pas avec l’PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Création d’un nœud de transformation à partir d’une table MFT

Pour créer un nœud de transformation à partir d’une table MFT, procédez comme suit :

1.  Créer une instance de la table MFT et obtenir un pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de la table MFT.
2.  Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ transformation \_ de topologie MF** pour créer le nœud de transformation.
3.  Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez le pointeur [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .
4.  Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.

L’exemple suivant crée et initialise un nœud de transformation à partir d’une table MFT.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a>Création d’un nœud de transformation à partir d’un CLSID

Pour créer un nœud de transformation à partir d’un CLSID, procédez comme suit :

1.  Recherche le CLSID de la table MFT. Vous pouvez utiliser la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) pour rechercher les CLSID de MFTS par catégorie, tels que les décodeurs ou les encodeurs. Vous pouvez également connaître le CLSID d’une table MFT particulière que vous souhaitez utiliser (par exemple, si vous avez implémenté votre propre MFT personnalisé).
2.  Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ transformation \_ de topologie MF** pour créer le nœud de transformation.
3.  Définissez l’attribut d' **\_ \_ \_ ObjectID de transformation TOPONODE MF** sur le nœud. La valeur de l’attribut est le CLSID.
4.  Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.

L’exemple suivant crée et initialise un nœud Transform à partir d’un CLSID.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a>Création d’un nœud de transformation à partir d’un objet d’activation

Certains MFTs fournissent des objets d’activation. Par exemple, la fonction [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) retourne un objet d’activation pour l’encodeur Windows Media audio (WMA). La fonction exact dépend de la table MFT. Toutes les MFT fournissent un objet d’activation. Pour plus d’informations, consultez [objets d’activation](activation-objects.md).

Vous pouvez également récupérer un objet d’activation MFT en appelant la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Pour créer un nœud de transformation à partir d’un objet d’activation, procédez comme suit :

1.  Créez l’objet d’activation et récupérez un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) de l’objet d’activation.
2.  Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ transformation \_ de topologie MF** pour créer le nœud de transformation.
3.  Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.

L’exemple suivant crée et initialise un nœud Transform à partir d’un objet d’activation.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de topologies](creating-topologies.md)
</dt> <dt>

[Topologies](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



