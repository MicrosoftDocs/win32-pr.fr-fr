---
description: Cette rubrique explique comment définir une heure d’arrêt pour la lecture lors de l’utilisation de la session multimédia.
ms.assetid: B8BA2154-2824-4573-AE71-853EB8AB911D
title: Comment définir l’heure d’arrêt de la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c14145f798795dfeb8116195afad2f020eb4219b9c2529f96b8fa904f2e1d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465999"
---
# <a name="how-to-set-the-playback-stop-time"></a>Comment définir l’heure d’arrêt de la lecture

Cette rubrique explique comment définir une heure d’arrêt pour la lecture lors de l’utilisation de la [session multimédia](media-session.md).

## <a name="setting-the-stop-time-before-playback-begins"></a>Définition de l’heure d’arrêt avant le début de la lecture

Avant de mettre en file d’attente une topologie pour la lecture, vous pouvez spécifier l’heure d’arrêt à l’aide de l’attribut [ \_ \_ MEDIASTOP MF TOPONODE](mf-toponode-mediastop-attribute.md) . Pour chaque nœud de sortie de la topologie, définissez la valeur de l' \_ TOPONODE MF \_ MEDIASTOP sur l’heure d’arrêt en unités de 100 nanosecondes.

Notez que la définition de cet attribut après le démarrage de la lecture n’a aucun effet. Par conséquent, définissez l’attribut avant d’appeler [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

Le code suivant montre comment définir l’heure d’arrêt sur une topologie existante.


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



## <a name="setting-the-stop-time-after-playback-has-started"></a>Définition de l’heure d’arrêt après le démarrage de la lecture

Il existe un moyen de définir l’heure d’arrêt après la lecture de la [session multimédia](media-session.md) à l’aide de l’interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) .

> [!IMPORTANT]
> Cette interface a une limitation sérieuse, car l’heure d’arrêt est spécifiée en tant que valeur 32 bits. Cela signifie que la durée maximale que vous pouvez définir à l’aide de cette interface est 0xFFFFFFFF, ou juste plus de 7 minutes. Cette limitation est due à une définition de structure incorrecte.

 

Pour définir l’heure d’arrêt à l’aide de l’interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) , procédez comme suit.

1.  Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer l’interface [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor) à partir de la session multimédia.
2.  Appelez [**IMFTopology :: GetTopologyID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid) pour connaître l’ID de la topologie de lecture.
3.  Pour chaque nœud de sortie de la topologie, appelez [**IMFTopologyNodeAttributeEditor :: UpdateNodeAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynodeattributeeditor-updatenodeattributes). Cette méthode prend l’ID de topologie et un pointeur vers une structure de [**\_ \_ mise à jour d’attribut MFTOPONODE**](/windows/desktop/api/mfidl/ns-mfidl-mftoponode_attribute_update) . Initialisez la structure comme suit.

    | Membre               | Valeur                                                                                                               |
    |----------------------|---------------------------------------------------------------------------------------------------------------------|
    | **NodeId**           | ID du nœud. Pour récupérer l’ID du nœud, appelez [**IMFTopologyNode :: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid). |
    | **guidAttributeKey** | **\_MEDIASTOP TOPONODE \_ MF**                                                                                         |
    | **attrType**         | **\_Attribut MF \_ UINT64**                                                                                           |
    | **u64**              | Heure d’arrêt, en unités de 100 nanosecondes.                                                                             |

    

     

Veillez à définir correctement la valeur de **attrType** . Bien que **U64** soit un type 32 bits, la méthode exige que **attrType** soit défini sur **l' \_ attribut MF \_ UINT64**.

Le code suivant illustre ces étapes.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> </dl>

 

 



