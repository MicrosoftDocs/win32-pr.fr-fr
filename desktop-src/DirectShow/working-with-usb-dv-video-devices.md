---
description: Utilisation des périphériques vidéo USB DV
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Utilisation des périphériques vidéo USB DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999573"
---
# <a name="working-with-usb-dv-video-devices"></a>Utilisation des périphériques vidéo USB DV

Cette rubrique explique comment écrire des applications pour les périphériques vidéo USB (Universal Serial Bus) qui capturent la vidéo DV.

Le format DV standard a une vitesse de données d’environ 25 mégabits par seconde (Mbits/s). Lors de la première introduction de l’USB, la bande passante est insuffisante pour prendre en charge la vidéo DV. Toutefois, USB 2,0 peut prendre en charge jusqu’à 480 Mbits/s, ce qui est plus que suffisant pour la vidéo DV. La spécification UVC (USB Video Device Class), publiée dans 2003, définit le format de charge utile pour les périphériques vidéo USB DV. un pilote de classe Windows Driver Model (WDM) pour les appareils UVC a été introduit dans Windows XP Service Pack 2.

Dans la plupart des cas, le pilote UVC prend en charge le même modèle de programmation que le pilote MSDV pour les appareils IEEE 1394. Les applications écrites pour MSDV doivent uniquement nécessiter des modifications mineures pour prendre en charge les appareils UVC.

Le pilote UVC se comporte différemment du pilote MSDV dans les domaines suivants :

-   [Modèle d’appareil](device-mode.md)
-   [Format de flux](stream-format.md)
-   [Format de signal](signal-format.md)
-   [Recherche de l’emplacement de la bande](tape-location-search.md)
-   [Transmettez le fichier DV du fichier à la bande](transmit-dv-from-file-to-tape.md).

Pour déterminer le pilote utilisé, appelez [**IAMExtDevice :: obtenir \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport). Le pilote MSDV retourne l' \_ indicateur de port dev \_ 1394 et le pilote UVC renvoie l' \_ indicateur USB du port dev \_ .

**Nœuds d’appareil**

Dans la terminologie USB, les points de terminaison sont les points où les données entrent ou quittent l’appareil. Un point de terminaison a une direction de Data Flow, qu’il s’agisse d’une entrée (de l’appareil à l’hôte) ou d’une sortie (de l’hôte au périphérique). Il peut être utile de considérer ces instructions comme étant relatives à l’hôte. L’entrée va à l’hôte ; la sortie provient de l’hôte. Le diagramme suivant illustre les deux points de terminaison.

![points de terminaison USB](images/ksnodes01.png)

Dans un appareil UVC, les fonctions de l’appareil sont logiquement divisées en composants appelés unités et terminaux. Une unité reçoit un ou plusieurs flux de données en tant qu’entrée et remet exactement un flux comme sortie. Un terminal est le point de départ ou le point de fin d’un flux de données. Les points de terminaison USB correspondent aux terminaux, mais les directions sont inversées : un point de terminaison d’entrée est représenté par un terminal de sortie, et vice versa. Le diagramme suivant illustre la relation entre les terminaux et les points de terminaison.

![unités et terminaux UVC](images/ksnodes02.png)

En outre, tous les terminaux ne correspondent pas à un point de terminaison USB. Le terme point de terminaison fait spécifiquement référence aux connexions USB et un périphérique peut envoyer ou recevoir des données via des connexions non-USB. Par exemple, une caméra vidéo est un terminal d’entrée et un écran LCD est un terminal de sortie.

Dans le filtre de proxy KS, les unités et les terminaux sont représentés sous forme de nœuds à l’intérieur du filtre. Le terme nœud est plus général que les termes unité et terminal, car les périphériques non-USB peuvent également avoir des nœuds. Pour obtenir des informations sur les nœuds d’un filtre, interrogez le filtre de l’interface [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) . Les types de nœuds sont identifiés par des GUID. Les nœuds sélecteur sont des nœuds qui peuvent basculer entre deux ou plusieurs entrées. Les nœuds sélecteur exposent l’interface [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) .

Le code suivant teste si une broche de sortie sur un filtre reçoit l’entrée d’un nœud d’un type donné.


```C++
// Structure to hold topology information.
struct TopologyConnections
{
    KSTOPOLOGY_CONNECTION *connections; // Array of connections
    DWORD count;  // Number of elements in the array
};

/////////////////////////////////////////////////////////////////////
// Name: GetTopologyConnections
// Desc: Gets the topology information from a filter.
//
// pTopo:       Pointer to the filter's IKsTopologyInfo interface.
// connectInfo: Pointer to a TopologyConnections structure. The 
//              function fills in this structure.
//
// Note: If the function succeeds, call CoTaskMemFree to free the
//       pConnectInfo->connections array.
/////////////////////////////////////////////////////////////////////

HRESULT GetTopologyConnections(
    IKsTopologyInfo *pTopo, 
    TopologyConnections *pConnectInfo
    )
{
    DWORD count;
    HRESULT hr = pTopo->get_NumConnections(&count);
    if (FAILED(hr))
    {
        return hr;
    }

    pConnectInfo->count = count;
    pConnectInfo->connections = NULL;
    if (count > 0)
    {
        // Allocate an array for the connection information.
        SIZE_T cb = sizeof(KSTOPOLOGY_CONNECTION) * count;
        KSTOPOLOGY_CONNECTION *pConnections = 
            (KSTOPOLOGY_CONNECTION*) CoTaskMemAlloc(cb);
        if (pConnections == NULL)
        {
            return E_OUTOFMEMORY;
        }
        // Fill the array.
        for (DWORD ix = 0; ix < count; ix++)
        {
            hr = pTopo->get_ConnectionInfo(ix, &pConnections[ix]);
            if (FAILED(hr))
            {
                break;
            }
        }
        if (SUCCEEDED(hr))
        {
            pConnectInfo->connections = pConnections;
        }
        else
        {
           CoTaskMemFree(pConnections);
        }
    }
    return hr;
}

/////////////////////////////////////////////////////////////////////
// Name: IsNodeDownstreamFromNode
// Desc: Searches upstream from a node for a specified node type.
//
// pTopo:        Pointer to the filter's IKsTopologyInfo interface.
// connectInfo:  Contains toplogy information. To fill in this
//               structure, call GetTopologyConnections.
// nodeID:       ID of the starting node in the search.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected, or false otherwise.
//
// Note: If the source node matches the type, this function returns 
//       true without searching upstream.
/////////////////////////////////////////////////////////////////////

HRESULT IsNodeDownstreamFromNode(
    IKsTopologyInfo *pTopo,
    const TopologyConnections& connectInfo, 
    DWORD nodeID,
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    *pIsConnected = false;
    // Base case for recursion: check the source node.
    GUID type;
    HRESULT hr = pTopo->get_NodeType(nodeID, &type);
    if (FAILED(hr))
    {
        return hr;
    }
    if (type == nodeType)
    {
        *pIsConnected = true;
        return S_OK;
    }

    // If the source node is a selector, get the input node.
    CComPtr<ISelector> pSelector;
    hr = pTopo->CreateNodeInstance(nodeID, __uuidof(ISelector), 
        (void**)&pSelector);
    if (SUCCEEDED(hr))
    {
        DWORD sourceNodeID;
        hr = pSelector->get_SourceNodeId(&sourceNodeID);
        if (SUCCEEDED(hr))
        {
            // Recursive call with the selector's input node.
            return IsNodeDownstreamFromNode(pTopo, connectInfo, 
                       sourceNodeID, nodeType, pIsConnected);
        }
    }
    else if (hr == E_NOINTERFACE)
    {
        hr = S_OK;  // This node is not a selector. Not a failure.
    }
    else
    {
        return hr;
    }

    // Test all of the upstream connections on this pin. 
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == nodeID) &&
            (connectInfo.connections[ix].FromNode != KSFILTER_NODE))
        {
            // FromNode is connected to the source node.
            DWORD fromNode = connectInfo.connections[ix].FromNode;

            // Recursive call with the upstream node.
            bool bIsConnected;
            hr = IsNodeDownstreamFromNode(pTopo, connectInfo, 
                fromNode, nodeType, &bIsConnected);
            if (FAILED(hr))
            {
                break;
            }
            if (bIsConnected)
            {
                *pIsConnected = true;
                break;
            }
        }
    }
    return hr;
}


/////////////////////////////////////////////////////////////////////
// Name: GetNodeUpstreamFromPin
// Desc: Finds the node connected to an output pin.
//
// connectInfo: Contains toplogy information. To fill in this
//              structure, call GetTopologyConnections.
// nPinIndex:   Index of the output pin.
// pNodeID:     Receives the ID of the connected node.
/////////////////////////////////////////////////////////////////////

HRESULT GetNodeUpstreamFromPin(
    const TopologyConnections& connectInfo, 
    UINT nPinIndex, 
    DWORD *pNodeID
    )
{
    bool bFound = false;
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == KSFILTER_NODE) &&
            (connectInfo.connections[ix].ToNodePin == nPinIndex))
        {
            *pNodeID = connectInfo.connections[ix].FromNode;
            bFound = true;
            break;
        }
    }
    if (bFound)
    {
        return S_OK;
    }
    else
    {
        return E_FAIL;
    }
}


/////////////////////////////////////////////////////////////////////
// Name: IsPinDownstreamFromNode
// Desc: Tests whether an output pin gets data from a node of
//       a specified type.
// 
// pFilter:      Pointer to the filter's IBaseFilter interface.
// UINT:         Index of the output pin to test.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected; false otherwise.
/////////////////////////////////////////////////////////////////////

HRESULT IsPinDownstreamFromNode(
    IBaseFilter *pFilter, 
    UINT nPinIndex, 
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    CComQIPtr<IKsTopologyInfo> pTopo(pFilter);
    if (pTopo == NULL)
    {
        return E_NOINTERFACE;
    }

    // Get the topology connection information.
    TopologyConnections connectionInfo;
    HRESULT hr = GetTopologyConnections(pTopo, &connectionInfo);
    if (FAILED(hr))
    {
        return hr;
    }

    // Find the node upstream from this pin.
    DWORD nodeID;
    hr = GetNodeUpstreamFromPin(connectionInfo, nPinIndex, &nodeID);
    if (SUCCEEDED(hr))
    {
        bool isConnected;
        hr = IsNodeDownstreamFromNode(pTopo, connectionInfo, 
            nodeID, nodeType, &isConnected);
        if (SUCCEEDED(hr))
        {
            *pIsConnected = isConnected;
        }
    }
    CoTaskMemFree(connectionInfo.connections);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



