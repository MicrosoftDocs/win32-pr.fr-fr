---
description: Cette rubrique explique comment définir une heure d’arrêt pour la lecture lors de l’utilisation de la session multimédia.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Comment définir l’heure d’arrêt de la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65269260b1e40d7907f0233fad653deb9636848b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518578"
---
# <a name="how-to-set-the-playback-stop-time"></a><span data-ttu-id="136b9-103">Comment définir l’heure d’arrêt de la lecture</span><span class="sxs-lookup"><span data-stu-id="136b9-103">How to Set the Playback Stop Time</span></span>

<span data-ttu-id="136b9-104">Cette rubrique explique comment définir une heure d’arrêt pour la lecture lors de l’utilisation de la [session multimédia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="136b9-104">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span>

## <a name="setting-the-stop-time-before-playback-begins"></a><span data-ttu-id="136b9-105">Définition de l’heure d’arrêt avant le début de la lecture</span><span class="sxs-lookup"><span data-stu-id="136b9-105">Setting the Stop Time Before Playback Begins</span></span>

<span data-ttu-id="136b9-106">Avant de mettre en file d’attente une topologie pour la lecture, vous pouvez spécifier l’heure d’arrêt à l’aide de l’attribut [ \_ \_ MEDIASTOP MF TOPONODE](mf-toponode-mediastop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="136b9-106">Before you queue a topology for playback, you can specify the stop time by using the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute.</span></span> <span data-ttu-id="136b9-107">Pour chaque nœud de sortie de la topologie, définissez la valeur de l' \_ TOPONODE MF \_ MEDIASTOP sur l’heure d’arrêt en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="136b9-107">For each output node in the topology, set the value of the MF\_TOPONODE\_MEDIASTOP to the stop time in 100-nanosecond units.</span></span>

<span data-ttu-id="136b9-108">Notez que la définition de cet attribut après le démarrage de la lecture n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="136b9-108">Note that setting this attribute after playback starts has no effect.</span></span> <span data-ttu-id="136b9-109">Par conséquent, définissez l’attribut avant d’appeler [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="136b9-109">Therefore, set the attribute before calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

<span data-ttu-id="136b9-110">Le code suivant montre comment définir l’heure d’arrêt sur une topologie existante.</span><span class="sxs-lookup"><span data-stu-id="136b9-110">The following code shows how to set the stop time on an existing topology.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection->GetElement(dwIndex, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk->Release();
    }
    return hr;
}

HRESULT SetMediaStop(IMFTopology *pTopology, const LONGLONG& stop)
{
    IMFCollection *pCol = NULL;
    DWORD cNodes;

    HRESULT hr = pTopology->GetSourceNodeCollection(&pCol);
    if (SUCCEEDED(hr))
    {
        hr = pCol->GetElementCount(&cNodes);
    }
    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cNodes; i++)
        {
            IMFTopologyNode *pNode;
            hr = GetCollectionObject(pCol, i, &pNode);
            if (SUCCEEDED(hr))
            {
                pNode->SetUINT64(MF_TOPONODE_MEDIASTOP, stop);
            }
            pNode->Release();
        }
    }
    SafeRelease(&pCol);
    return hr;
}
```



## <a name="setting-the-stop-time-after-playback-has-started"></a><span data-ttu-id="136b9-111">Définition de l’heure d’arrêt après le démarrage de la lecture</span><span class="sxs-lookup"><span data-stu-id="136b9-111">Setting the Stop Time After Playback Has Started</span></span>

<span data-ttu-id="136b9-112">Il existe un moyen de définir l’heure d’arrêt après la lecture de la [session multimédia](media-session.md) à l’aide de l’interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .</span><span class="sxs-lookup"><span data-stu-id="136b9-112">There is a way to set the stop time after the [Media Session](media-session.md) starts playback, by using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="136b9-113">Cette interface a une limitation sérieuse, car l’heure d’arrêt est spécifiée en tant que valeur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="136b9-113">This interface has a serious limitation, because the stop time is specified as a 32-bit value.</span></span> <span data-ttu-id="136b9-114">Cela signifie que la durée maximale que vous pouvez définir à l’aide de cette interface est 0xFFFFFFFF, ou juste plus de 7 minutes.</span><span class="sxs-lookup"><span data-stu-id="136b9-114">That means the maximum stop time that you can set using this interface is 0xFFFFFFFF, or just over 7 minutes.</span></span> <span data-ttu-id="136b9-115">Cette limitation est due à une définition de structure incorrecte.</span><span class="sxs-lookup"><span data-stu-id="136b9-115">This limitation is due to an incorrect structure definition.</span></span>

 

<span data-ttu-id="136b9-116">Pour définir l’heure d’arrêt à l’aide de l’interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="136b9-116">To set the stop time using the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface, perform the following steps.</span></span>

1.  <span data-ttu-id="136b9-117">Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer l’interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="136b9-117">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) interface from the Media Session.</span></span>
2.  <span data-ttu-id="136b9-118">Appelez [**IMFTopology :: GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) pour connaître l’ID de la topologie de lecture.</span><span class="sxs-lookup"><span data-stu-id="136b9-118">Call [**IMFTopology::GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) to get the ID of the playback topology.</span></span>
3.  <span data-ttu-id="136b9-119">Pour chaque nœud de sortie de la topologie, appelez [**IMFTopologyNodeAttributeEditor :: UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span><span class="sxs-lookup"><span data-stu-id="136b9-119">For each output node in the topology, call [**IMFTopologyNodeAttributeEditor::UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes).</span></span> <span data-ttu-id="136b9-120">Cette méthode prend l’ID de topologie et un pointeur vers une structure de [**\_ \_ mise à jour d’attribut MFTOPONODE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) .</span><span class="sxs-lookup"><span data-stu-id="136b9-120">This method takes the topology ID and a pointer to a [**MFTOPONODE\_ATTRIBUTE\_UPDATE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) structure.</span></span> <span data-ttu-id="136b9-121">Initialisez la structure comme suit.</span><span class="sxs-lookup"><span data-stu-id="136b9-121">Initialize the structure as follows.</span></span>

    | <span data-ttu-id="136b9-122">Membre</span><span class="sxs-lookup"><span data-stu-id="136b9-122">Member</span></span>               | <span data-ttu-id="136b9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="136b9-123">Value</span></span>                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="136b9-124">**NodeId**</span><span class="sxs-lookup"><span data-stu-id="136b9-124">**NodeId**</span></span>           | <span data-ttu-id="136b9-125">ID du nœud.</span><span class="sxs-lookup"><span data-stu-id="136b9-125">The node ID.</span></span> <span data-ttu-id="136b9-126">Pour récupérer l’ID du nœud, appelez [**IMFTopologyNode :: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="136b9-126">To get the node ID, call call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span> |
    | <span data-ttu-id="136b9-127">**guidAttributeKey**</span><span class="sxs-lookup"><span data-stu-id="136b9-127">**guidAttributeKey**</span></span> | <span data-ttu-id="136b9-128">**\_MEDIASTOP TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="136b9-128">**MF\_TOPONODE\_MEDIASTOP**</span></span>                                                                                         |
    | <span data-ttu-id="136b9-129">**attrType**</span><span class="sxs-lookup"><span data-stu-id="136b9-129">**attrType**</span></span>         | <span data-ttu-id="136b9-130">**\_Attribut MF \_ UINT64**</span><span class="sxs-lookup"><span data-stu-id="136b9-130">**MF\_ATTRIBUTE\_UINT64**</span></span>                                                                                           |
    | <span data-ttu-id="136b9-131">**u64**</span><span class="sxs-lookup"><span data-stu-id="136b9-131">**u64**</span></span>              | <span data-ttu-id="136b9-132">Heure d’arrêt, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="136b9-132">The stop time, in 100-nanosecond units.</span></span>                                                                             |

    

     

<span data-ttu-id="136b9-133">Veillez à définir correctement la valeur de **attrType** .</span><span class="sxs-lookup"><span data-stu-id="136b9-133">Be careful to set the value of **attrType** correctly.</span></span> <span data-ttu-id="136b9-134">Bien que **U64** soit un type 32 bits, la méthode exige que **attrType** soit défini sur **l' \_ attribut MF \_ UINT64**.</span><span class="sxs-lookup"><span data-stu-id="136b9-134">Although **u64** is a 32-bit type, the method requires that **attrType** be set to **MF\_ATTRIBUTE\_UINT64**.</span></span>

<span data-ttu-id="136b9-135">Le code suivant illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="136b9-135">The following code shows these steps.</span></span>


```C++
HRESULT SetMediaStopDynamic(IMFMediaSession *pSession, IMFTopology *pTopology, const LONGLONG& stop)
{
    if (stop > MAXUINT32)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNodeAttributeEditor *pAttr = NULL;
    IMFCollection *pCol = NULL;
    IMFTopologyNode *pNode = NULL;

    HRESULT hr = MFGetService(pSession, MF_TOPONODE_ATTRIBUTE_EDITOR_SERVICE, IID_PPV_ARGS(&pAttr));
    if (FAILED(hr))
    {
        goto done;
    }

    TOPOID id;
    hr = pTopology->GetTopologyID(&id);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cNodes;
    hr = pTopology->GetSourceNodeCollection(&pCol);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pCol->GetElementCount(&cNodes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cNodes; i++)
    {
        IMFTopologyNode *pNode;
        hr = GetCollectionObject(pCol, i, &pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        TOPOID nodeID;
        hr = pNode->GetTopoNodeID(&nodeID);
        if (FAILED(hr))
        {
            goto done;
        }

        MFTOPONODE_ATTRIBUTE_UPDATE update;
        update.NodeId = nodeID;
        update.guidAttributeKey = MF_TOPONODE_MEDIASTOP;
        update.attrType = MF_ATTRIBUTE_UINT64;
        update.u64 = (UINT32)stop;

        hr = pAttr->UpdateNodeAttributes(id, 1, &update);
        if (FAILED(hr))
        {
            goto done;
        }
        SafeRelease(&pNode);
    }

done:
    SafeRelease(&pNode);
    SafeRelease(&pCol);
    SafeRelease(&pAttr);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="136b9-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="136b9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="136b9-137">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="136b9-137">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



