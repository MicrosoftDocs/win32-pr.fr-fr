---
description: Utilisation des périphériques vidéo USB DV
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Utilisation des périphériques vidéo USB DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201837"
---
# <a name="working-with-usb-dv-video-devices"></a><span data-ttu-id="0cf37-103">Utilisation des périphériques vidéo USB DV</span><span class="sxs-lookup"><span data-stu-id="0cf37-103">Working with USB DV Video Devices</span></span>

<span data-ttu-id="0cf37-104">Cette rubrique explique comment écrire des applications pour les périphériques vidéo USB (Universal Serial Bus) qui capturent la vidéo DV.</span><span class="sxs-lookup"><span data-stu-id="0cf37-104">This topic describes how to write applications for Universal Serial Bus (USB) video devices that capture DV video.</span></span>

<span data-ttu-id="0cf37-105">Le format DV standard a une vitesse de données d’environ 25 mégabits par seconde (Mbits/s).</span><span class="sxs-lookup"><span data-stu-id="0cf37-105">Standard DV format has a data rate of about 25 megabits per second (Mbps).</span></span> <span data-ttu-id="0cf37-106">Lors de la première introduction de l’USB, la bande passante est insuffisante pour prendre en charge la vidéo DV.</span><span class="sxs-lookup"><span data-stu-id="0cf37-106">When USB was first introduced, it did not have enough bandwidth to support DV video.</span></span> <span data-ttu-id="0cf37-107">Toutefois, USB 2,0 peut prendre en charge jusqu’à 480 Mbits/s, ce qui est plus que suffisant pour la vidéo DV.</span><span class="sxs-lookup"><span data-stu-id="0cf37-107">However, USB 2.0 can support up to 480 Mbps, which is more than sufficient for DV video.</span></span> <span data-ttu-id="0cf37-108">La spécification UVC (USB Video Device Class), publiée dans 2003, définit le format de charge utile pour les périphériques vidéo USB DV.</span><span class="sxs-lookup"><span data-stu-id="0cf37-108">The USB Video Device Class (UVC) specification, released in 2003, defines the payload format for USB DV video devices.</span></span> <span data-ttu-id="0cf37-109">Un pilote de classe Windows Driver Model (WDM) pour les appareils UVC a été introduit dans Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="0cf37-109">A Windows Driver Model (WDM) class driver for UVC devices was introduced in Windows XP Service Pack 2.</span></span>

<span data-ttu-id="0cf37-110">Dans la plupart des cas, le pilote UVC prend en charge le même modèle de programmation que le pilote MSDV pour les appareils IEEE 1394.</span><span class="sxs-lookup"><span data-stu-id="0cf37-110">In most respects, the UVC driver supports the same programming model as the MSDV driver for IEEE 1394 devices.</span></span> <span data-ttu-id="0cf37-111">Les applications écrites pour MSDV doivent uniquement nécessiter des modifications mineures pour prendre en charge les appareils UVC.</span><span class="sxs-lookup"><span data-stu-id="0cf37-111">Applications written for MSDV should require only minor modifications to support UVC devices.</span></span>

<span data-ttu-id="0cf37-112">Le pilote UVC se comporte différemment du pilote MSDV dans les domaines suivants :</span><span class="sxs-lookup"><span data-stu-id="0cf37-112">The UVC driver behaves differently from the MSDV driver in the following areas:</span></span>

-   [<span data-ttu-id="0cf37-113">Modèle d’appareil</span><span class="sxs-lookup"><span data-stu-id="0cf37-113">Device Mode</span></span>](device-mode.md)
-   [<span data-ttu-id="0cf37-114">Format de flux</span><span class="sxs-lookup"><span data-stu-id="0cf37-114">Stream Format</span></span>](stream-format.md)
-   [<span data-ttu-id="0cf37-115">Format de signal</span><span class="sxs-lookup"><span data-stu-id="0cf37-115">Signal Format</span></span>](signal-format.md)
-   [<span data-ttu-id="0cf37-116">Recherche de l’emplacement de la bande</span><span class="sxs-lookup"><span data-stu-id="0cf37-116">Tape Location Search</span></span>](tape-location-search.md)
-   <span data-ttu-id="0cf37-117">[Transmettez le fichier DV du fichier à la bande](transmit-dv-from-file-to-tape.md).</span><span class="sxs-lookup"><span data-stu-id="0cf37-117">[Transmit DV from File to Tape](transmit-dv-from-file-to-tape.md).</span></span>

<span data-ttu-id="0cf37-118">Pour déterminer le pilote utilisé, appelez [**IAMExtDevice :: obtenir \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span><span class="sxs-lookup"><span data-stu-id="0cf37-118">To determine which driver is being used, call [**IAMExtDevice::get\_DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span></span> <span data-ttu-id="0cf37-119">Le pilote MSDV retourne l' \_ indicateur de port dev \_ 1394 et le pilote UVC renvoie l' \_ indicateur USB du port dev \_ .</span><span class="sxs-lookup"><span data-stu-id="0cf37-119">The MSDV driver returns the DEV\_PORT\_1394 flag, and the UVC driver returns the DEV\_PORT\_USB flag.</span></span>

<span data-ttu-id="0cf37-120">**Nœuds d’appareil**</span><span class="sxs-lookup"><span data-stu-id="0cf37-120">**Device Nodes**</span></span>

<span data-ttu-id="0cf37-121">Dans la terminologie USB, les points de terminaison sont les points où les données entrent ou quittent l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0cf37-121">In USB terminology, endpoints are the points where data enters or leaves the device.</span></span> <span data-ttu-id="0cf37-122">Un point de terminaison a une direction de Data Flow, qu’il s’agisse d’une entrée (de l’appareil à l’hôte) ou d’une sortie (de l’hôte au périphérique).</span><span class="sxs-lookup"><span data-stu-id="0cf37-122">An endpoint has a direction of data flow, either input (from device to host) or output (from host to device).</span></span> <span data-ttu-id="0cf37-123">Il peut être utile de considérer ces instructions comme étant relatives à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="0cf37-123">It may help to think of these directions as being relative to the host.</span></span> <span data-ttu-id="0cf37-124">L’entrée va à l’hôte ; la sortie provient de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="0cf37-124">Input goes to the host; output comes from the host.</span></span> <span data-ttu-id="0cf37-125">Le diagramme suivant illustre les deux points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0cf37-125">The following diagram illustrates the two endpoints.</span></span>

![points de terminaison USB](images/ksnodes01.png)

<span data-ttu-id="0cf37-127">Dans un appareil UVC, les fonctions de l’appareil sont logiquement divisées en composants appelés unités et terminaux.</span><span class="sxs-lookup"><span data-stu-id="0cf37-127">In a UVC device, the functions of the device are logically divided into components called units and terminals.</span></span> <span data-ttu-id="0cf37-128">Une unité reçoit un ou plusieurs flux de données en tant qu’entrée et remet exactement un flux comme sortie.</span><span class="sxs-lookup"><span data-stu-id="0cf37-128">A unit receives one or more data streams as input and delivers exactly one stream as output.</span></span> <span data-ttu-id="0cf37-129">Un terminal est le point de départ ou le point de fin d’un flux de données.</span><span class="sxs-lookup"><span data-stu-id="0cf37-129">A terminal is the starting point or ending point for a data stream.</span></span> <span data-ttu-id="0cf37-130">Les points de terminaison USB correspondent aux terminaux, mais les directions sont inversées : un point de terminaison d’entrée est représenté par un terminal de sortie, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="0cf37-130">USB endpoints correspond to terminals, but the directions are reversed: an input endpoint is represented by an output terminal, and vice versa.</span></span> <span data-ttu-id="0cf37-131">Le diagramme suivant illustre la relation entre les terminaux et les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0cf37-131">The following diagram shows the relation between terminals and endpoints.</span></span>

![unités et terminaux UVC](images/ksnodes02.png)

<span data-ttu-id="0cf37-133">En outre, tous les terminaux ne correspondent pas à un point de terminaison USB.</span><span class="sxs-lookup"><span data-stu-id="0cf37-133">Also, not every terminal corresponds to a USB endpoint.</span></span> <span data-ttu-id="0cf37-134">Le terme point de terminaison fait spécifiquement référence aux connexions USB et un périphérique peut envoyer ou recevoir des données via des connexions non-USB.</span><span class="sxs-lookup"><span data-stu-id="0cf37-134">The term endpoint refers specifically to USB connections, and a device may send or receive data through non-USB connections.</span></span> <span data-ttu-id="0cf37-135">Par exemple, une caméra vidéo est un terminal d’entrée et un écran LCD est un terminal de sortie.</span><span class="sxs-lookup"><span data-stu-id="0cf37-135">For example, a video camera is an input terminal and an LCD screen is an output terminal.</span></span>

<span data-ttu-id="0cf37-136">Dans le filtre de proxy KS, les unités et les terminaux sont représentés sous forme de nœuds à l’intérieur du filtre.</span><span class="sxs-lookup"><span data-stu-id="0cf37-136">In the KS Proxy filter, units and terminals are represented as nodes inside the filter.</span></span> <span data-ttu-id="0cf37-137">Le terme nœud est plus général que les termes unité et terminal, car les périphériques non-USB peuvent également avoir des nœuds.</span><span class="sxs-lookup"><span data-stu-id="0cf37-137">The term node is more general than the terms unit and terminal because non-USB devices can also have nodes.</span></span> <span data-ttu-id="0cf37-138">Pour obtenir des informations sur les nœuds d’un filtre, interrogez le filtre de l’interface [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .</span><span class="sxs-lookup"><span data-stu-id="0cf37-138">To get information about the nodes in a filter, query the filter for the [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) interface.</span></span> <span data-ttu-id="0cf37-139">Les types de nœuds sont identifiés par des GUID.</span><span class="sxs-lookup"><span data-stu-id="0cf37-139">Node types are identified by GUIDs.</span></span> <span data-ttu-id="0cf37-140">Les nœuds sélecteur sont des nœuds qui peuvent basculer entre deux ou plusieurs entrées.</span><span class="sxs-lookup"><span data-stu-id="0cf37-140">Selector nodes are nodes that can switch between two or more inputs.</span></span> <span data-ttu-id="0cf37-141">Les nœuds sélecteur exposent l’interface [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) .</span><span class="sxs-lookup"><span data-stu-id="0cf37-141">Selector nodes expose the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface.</span></span>

<span data-ttu-id="0cf37-142">Le code suivant teste si une broche de sortie sur un filtre reçoit l’entrée d’un nœud d’un type donné.</span><span class="sxs-lookup"><span data-stu-id="0cf37-142">The following code tests whether an output pin on a filter receives input from a node of a given type.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0cf37-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cf37-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cf37-144">Vidéo numérique dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="0cf37-144">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



