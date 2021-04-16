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
# <a name="creating-transform-nodes"></a><span data-ttu-id="c1674-103">Création de nœuds de transformation</span><span class="sxs-lookup"><span data-stu-id="c1674-103">Creating Transform Nodes</span></span>

<span data-ttu-id="c1674-104">Un nœud de transformation représente une Media Foundation transformation (MFT), telle qu’un décodeur ou un encodeur.</span><span class="sxs-lookup"><span data-stu-id="c1674-104">A transform node represents a Media Foundation transform (MFT), such as a decoder or encoder.</span></span> <span data-ttu-id="c1674-105">Il existe plusieurs façons d’initialiser un nœud transformer :</span><span class="sxs-lookup"><span data-stu-id="c1674-105">There are several different ways to initialize a transform node:</span></span>

-   <span data-ttu-id="c1674-106">À partir d’un pointeur vers la table MFT.</span><span class="sxs-lookup"><span data-stu-id="c1674-106">From a pointer to the MFT.</span></span>
-   <span data-ttu-id="c1674-107">À partir d’un CLSID pour la table MFT.</span><span class="sxs-lookup"><span data-stu-id="c1674-107">From a CLSID for the MFT.</span></span>
-   <span data-ttu-id="c1674-108">À partir d’un pointeur vers un objet d’activation pour la table MFT.</span><span class="sxs-lookup"><span data-stu-id="c1674-108">From a pointer to an activation object for the MFT.</span></span>

<span data-ttu-id="c1674-109">Si vous envisagez de charger la topologie à l’intérieur du chemin d’accès de média protégé (PMP), vous devez utiliser le CLSID ou un objet d’activation, afin que la table MFT puisse être créée à l’intérieur du processus protégé.</span><span class="sxs-lookup"><span data-stu-id="c1674-109">If you are going to load the topology inside the protected media path (PMP), you must use either the CLSID or an activation object, so that the MFT can be created inside the protected process.</span></span> <span data-ttu-id="c1674-110">La première approche (à l’aide d’un pointeur vers la table MFT) ne fonctionne pas avec l’PMP.</span><span class="sxs-lookup"><span data-stu-id="c1674-110">The first approach (using a pointer to the MFT) does not work with the PMP.</span></span>

## <a name="creating-a-transform-node-from-an-mft"></a><span data-ttu-id="c1674-111">Création d’un nœud de transformation à partir d’une table MFT</span><span class="sxs-lookup"><span data-stu-id="c1674-111">Creating a Transform Node from an MFT</span></span>

<span data-ttu-id="c1674-112">Pour créer un nœud de transformation à partir d’une table MFT, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c1674-112">To create a transform node from an MFT, do the following:</span></span>

1.  <span data-ttu-id="c1674-113">Créer une instance de la table MFT et obtenir un pointeur vers l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="c1674-113">Create an instance of the MFT and get a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the MFT.</span></span>
2.  <span data-ttu-id="c1674-114">Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ transformation \_ de topologie MF** pour créer le nœud de transformation.</span><span class="sxs-lookup"><span data-stu-id="c1674-114">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="c1674-115">Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez le pointeur [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="c1674-115">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer.</span></span>
4.  <span data-ttu-id="c1674-116">Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.</span><span class="sxs-lookup"><span data-stu-id="c1674-116">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="c1674-117">L’exemple suivant crée et initialise un nœud de transformation à partir d’une table MFT.</span><span class="sxs-lookup"><span data-stu-id="c1674-117">The following example creates and initializes a transform node from an MFT.</span></span>


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



## <a name="creating-a-transform-node-from-a-clsid"></a><span data-ttu-id="c1674-118">Création d’un nœud de transformation à partir d’un CLSID</span><span class="sxs-lookup"><span data-stu-id="c1674-118">Creating a Transform Node from a CLSID</span></span>

<span data-ttu-id="c1674-119">Pour créer un nœud de transformation à partir d’un CLSID, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c1674-119">To create a transform node from a CLSID, do the following:</span></span>

1.  <span data-ttu-id="c1674-120">Recherche le CLSID de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="c1674-120">Find the CLSID of the MFT.</span></span> <span data-ttu-id="c1674-121">Vous pouvez utiliser la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) pour rechercher les CLSID de MFTS par catégorie, tels que les décodeurs ou les encodeurs.</span><span class="sxs-lookup"><span data-stu-id="c1674-121">You can use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to find the CLSIDs of MFTs by category, such as decoders or encoders.</span></span> <span data-ttu-id="c1674-122">Vous pouvez également connaître le CLSID d’une table MFT particulière que vous souhaitez utiliser (par exemple, si vous avez implémenté votre propre MFT personnalisé).</span><span class="sxs-lookup"><span data-stu-id="c1674-122">You might also know the CLSID of a particular MFT that you want to use (for example, if you implemented your own custom MFT).</span></span>
2.  <span data-ttu-id="c1674-123">Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ transformation \_ de topologie MF** pour créer le nœud de transformation.</span><span class="sxs-lookup"><span data-stu-id="c1674-123">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="c1674-124">Définissez l’attribut d' **\_ \_ \_ ObjectID de transformation TOPONODE MF** sur le nœud.</span><span class="sxs-lookup"><span data-stu-id="c1674-124">Set the **MF\_TOPONODE\_TRANSFORM\_OBJECTID** attribute on the node.</span></span> <span data-ttu-id="c1674-125">La valeur de l’attribut est le CLSID.</span><span class="sxs-lookup"><span data-stu-id="c1674-125">The attribute value is the CLSID.</span></span>
4.  <span data-ttu-id="c1674-126">Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.</span><span class="sxs-lookup"><span data-stu-id="c1674-126">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="c1674-127">L’exemple suivant crée et initialise un nœud Transform à partir d’un CLSID.</span><span class="sxs-lookup"><span data-stu-id="c1674-127">The following example creates and initializes a transform node from a CLSID.</span></span>


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



## <a name="creating-a-transform-node-from-an-activation-object"></a><span data-ttu-id="c1674-128">Création d’un nœud de transformation à partir d’un objet d’activation</span><span class="sxs-lookup"><span data-stu-id="c1674-128">Creating a Transform Node from an Activation Object</span></span>

<span data-ttu-id="c1674-129">Certains MFTs fournissent des objets d’activation.</span><span class="sxs-lookup"><span data-stu-id="c1674-129">Some MFTs provide activation objects.</span></span> <span data-ttu-id="c1674-130">Par exemple, la fonction [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) retourne un objet d’activation pour l’encodeur Windows Media audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="c1674-130">For example, the [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) function returns an activation object for the Windows Media Audio (WMA) encoder.</span></span> <span data-ttu-id="c1674-131">La fonction exact dépend de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="c1674-131">The exact function depends on the MFT.</span></span> <span data-ttu-id="c1674-132">Toutes les MFT fournissent un objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="c1674-132">Not every MFT provides an activation object.</span></span> <span data-ttu-id="c1674-133">Pour plus d’informations, consultez [objets d’activation](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c1674-133">For more information, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="c1674-134">Vous pouvez également récupérer un objet d’activation MFT en appelant la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="c1674-134">You can also get an MFT activation object by calling the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="c1674-135">Pour créer un nœud de transformation à partir d’un objet d’activation, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c1674-135">To create a transform node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="c1674-136">Créez l’objet d’activation et récupérez un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) de l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="c1674-136">Create the activation object and get a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the activation object.</span></span>
2.  <span data-ttu-id="c1674-137">Appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) avec l’indicateur de **\_ nœud de \_ transformation \_ de topologie MF** pour créer le nœud de transformation.</span><span class="sxs-lookup"><span data-stu-id="c1674-137">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="c1674-138">Appelez [**IMFTopologyNode :: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) et transmettez le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="c1674-138">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
4.  <span data-ttu-id="c1674-139">Appelez [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) pour ajouter le nœud à la topologie.</span><span class="sxs-lookup"><span data-stu-id="c1674-139">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="c1674-140">L’exemple suivant crée et initialise un nœud Transform à partir d’un objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="c1674-140">The following example creates and initializes a transform node from an activation object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c1674-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1674-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1674-142">Création de topologies</span><span class="sxs-lookup"><span data-stu-id="c1674-142">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="c1674-143">Topologies</span><span class="sxs-lookup"><span data-stu-id="c1674-143">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="c1674-144">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c1674-144">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



