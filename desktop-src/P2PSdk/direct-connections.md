---
description: Les infrastructures de représentation graphique et de regroupement d’homologues permettent aux applications de se connecter directement à un nœud (graphique) ou à un membre (regroupement), puis d’échanger des données directement avec le nœud. Cette connexion est appelée connexion directe.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Connexions directes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e357b3a4ebc765a013de05234bc8fc9be20943d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527480"
---
# <a name="direct-connections"></a><span data-ttu-id="c9a5b-104">Connexions directes</span><span class="sxs-lookup"><span data-stu-id="c9a5b-104">Direct Connections</span></span>

<span data-ttu-id="c9a5b-105">Les infrastructures de représentation graphique et de regroupement d’homologues permettent aux applications de se connecter directement à un nœud (graphique) ou à un membre (regroupement), puis d’échanger des données directement avec le nœud.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-105">The Peer Graphing and Peer Grouping Infrastructures allow applications to connect directly to one node (Graphing) or member (Grouping), and then exchange data directly with the node.</span></span> <span data-ttu-id="c9a5b-106">Cette connexion est appelée **connexion directe**.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-106">This connection is called a **direct connection**.</span></span>

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a><span data-ttu-id="c9a5b-107">Connexions directes à l’aide de l’infrastructure de représentation graphique des pairs</span><span class="sxs-lookup"><span data-stu-id="c9a5b-107">Direct Connections using the Peer Graphing Infrastructure</span></span>

<span data-ttu-id="c9a5b-108">Avant de pouvoir établir une connexion directe entre deux nœuds d’un graphique, les deux nœuds doivent être inscrits pour l’événement de **\_ \_ \_ \_ connexion directe d’événement de graphique pair à pair** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-108">Before a direct connection can be established between two nodes in a graph, both nodes must be registered for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="c9a5b-109">Pour recevoir des données via une connexion directe, les nœuds doivent également être inscrits pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement Graph pair** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-109">To receive data over a direct connection, the nodes must also be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="c9a5b-110">**Homologue \_ \_ \_ La \_ connexion directe** à un événement de graphique est un événement qui avertit une application qu’une tentative de connexion directe réussit ou échoue.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-110">**PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="c9a5b-111">L’état réel de réussite ou d’échec d’un appel à [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) est retourné dans la structure des [**données d' \_ événement du graphique \_ \_ homologue**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-111">The actual success or failure status of a call to [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) is returned in the [**PEER\_GRAPH\_EVENT\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) structure.</span></span>

<span data-ttu-id="c9a5b-112">Pour créer une connexion directe, une application appelle [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), puis passe un handle au graphique, un pointeur vers l’identité de l’autre nœud qui participe à la connexion et un pointeur vers une structure d’adresse IPv6 pour le nœud participant.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-112">To create a direct connection, an application calls [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), and then passes a handle to the graph, a pointer to the identity of the other node that is participating in the connection, and a pointer to an IPv6 address structure for the participating node.</span></span> <span data-ttu-id="c9a5b-113">L’identité du nœud et l’adresse IPv6 qui sont spécifiées dans l’appel à **PeerGraphOpenDirectConnection** doivent être inscrites pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement du graphique homologue** , ou ne peuvent pas recevoir les données envoyées par un homologue appelant.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-113">The node identity and IPv6 address that are specified in the call to **PeerGraphOpenDirectConnection** must be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event, or it cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="c9a5b-114">En cas de réussite, **PeerGraphOpenDirectConnection** retourne un ID de connexion 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-114">When successful, **PeerGraphOpenDirectConnection** returns a 64-bit connection ID.</span></span> <span data-ttu-id="c9a5b-115">Toutefois, l’homologue doit attendre l’événement de **\_ \_ \_ \_ connexion directe d’événement de groupe pair** avant que l’ID de connexion directe puisse être identifié comme valide.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-115">However, the peer must wait for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="c9a5b-116">Une fois qu’une connexion est établie et qu’un ID de connexion valide est confirmé, une application peut appeler [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) pour envoyer les données via la connexion spécifiée par l’ID de connexion valide à l’homologue participant, si l’homologue participant est inscrit pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement de graphique pair** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-116">After a connection is made and a valid connection ID is confirmed, an application can call [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) to send the data across the connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="c9a5b-117">Les données opaques sont disponibles sous la forme d’une structure de [**\_ données d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_data) dans les [**\_ \_ \_ données entrantes des événements homologues**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retournées par l’événement de **\_ \_ \_ \_ données entrantes de l’événement Graph pair** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-117">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="c9a5b-118">Quand une connexion n’est pas nécessaire, une application appelle [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) avec le descripteur de graphique et l’ID de connexion.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-118">When a connection is not needed, an application calls [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) with the graph handle and the connection ID.</span></span>

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a><span data-ttu-id="c9a5b-119">Connexions directes à l’aide de l’infrastructure de regroupement d’homologues</span><span class="sxs-lookup"><span data-stu-id="c9a5b-119">Direct Connections using the Peer Grouping Infrastructure</span></span>

<span data-ttu-id="c9a5b-120">Les connexions directes au sein de l’infrastructure de regroupement d’homologues sont gérées de la même façon que l’infrastructure de représentation graphique des homologues.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-120">Direct connections within the Peer Grouping Infrastructure are handled similar to the Peer Graphing Infrastructure.</span></span>

<span data-ttu-id="c9a5b-121">Avant de pouvoir établir une connexion directe entre deux membres d’un groupe, les deux membres doivent s’inscrire à l’événement de **\_ \_ \_ \_ connexion directe d’événement de groupe pair** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-121">Before a direct connection can be established between two members in a group, both members must register for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="c9a5b-122">Si un membre du groupe souhaite recevoir des données via une connexion directe, le membre du groupe doit également s’inscrire à l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe homologue** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-122">If a group member wants to receive data over a direct connection, the group member must also register for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="c9a5b-123">**Homologue \_ \_ \_ La \_ connexion directe d’événement de groupe** est un événement qui avertit une application qu’une tentative de connexion directe réussit ou échoue.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-123">**PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** is an event that is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="c9a5b-124">L’état réel de réussite ou d’échec d’un appel à [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) est retourné dans la structure [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-124">The actual success or failure status of a call to [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) is returned in the [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure.</span></span>

<span data-ttu-id="c9a5b-125">Pour créer une connexion directe, une application appelle [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), puis passe un handle au groupe, un pointeur vers l’identité de l’autre membre qui participera à cette connexion et un pointeur vers une structure d’adresse IPv6 pour le membre participant.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-125">To create a direct connection, an application calls [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), and then passes a handle to the group, a pointer to the identity of the other member that will participate in this connection, and a pointer to an IPv6 address structure for the participating member.</span></span> <span data-ttu-id="c9a5b-126">Le membre dont l’identité et l’adresse IPv6 sont spécifiées dans l’appel à **PeerGroupOpenDirectConnection** doivent être inscrits pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe homologue** , ou le membre ne peut pas recevoir les données envoyées par un homologue appelant.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-126">The member whose identity and IPv6 address are specified in the call to **PeerGroupOpenDirectConnection** must be registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event, or the member cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="c9a5b-127">**PeerGroupOpenDirectConnection** retourne un ID de connexion 64 bits en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-127">**PeerGroupOpenDirectConnection** returns a 64-bit connection ID when successful.</span></span> <span data-ttu-id="c9a5b-128">Toutefois, un homologue doit attendre que l’événement de **\_ \_ \_ \_ connexion directe d’événement de graphique pair** soit déclenché avant que l’ID de connexion directe puisse être identifié comme valide.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-128">However, a peer must wait for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event to be raised before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="c9a5b-129">Une fois qu’une connexion est établie et qu’un ID de connexion valide est confirmé, une application peut appeler [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) pour envoyer des données via une connexion spécifiée par l’ID de connexion valide à l’homologue participant, si l’homologue participant est inscrit pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe pair** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-129">After a connection is made and a valid connection ID is confirmed, then an application can call [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) to send data across a connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="c9a5b-130">Les données opaques sont disponibles en tant que structure de [**\_ données homologues**](/windows/desktop/api/P2P/ns-p2p-peer_data) dans les [**\_ \_ \_ données entrantes des événements homologues**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retournées par l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe pair** .</span><span class="sxs-lookup"><span data-stu-id="c9a5b-130">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="c9a5b-131">Lorsque la connexion n’est pas nécessaire, l’application appelle [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) avec le descripteur de groupe et l’ID de connexion.</span><span class="sxs-lookup"><span data-stu-id="c9a5b-131">When the connection is not needed, the application calls [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) with the group handle and the connection ID.</span></span>

## <a name="example-of-a-direct-connection-for-graphing"></a><span data-ttu-id="c9a5b-132">Exemple de connexion directe pour la représentation graphique</span><span class="sxs-lookup"><span data-stu-id="c9a5b-132">Example of a Direct Connection for Graphing</span></span>


```C++
#include <p2p.h>

#pragma comment(lib, "p2pgraph.lib")

//-----------------------------------------------------------------------------
// Function: CreateDirectConnection
//
// Purpose:  Demonstrate how to create a direct connection.
//
// Arguments:
//           hGraph - the graph in which to create the connection
//           pwzId  - the peer identification string
//
// Returns:  ULONGLONG - the connection id or 0
//

ULONGLONG CreateDirectConnection(HGRAPH hGraph, PCWSTR pwzId)
{
    HRESULT   hr = S_OK;

    ULONGLONG ullConnection = 0; // the connection id to return

    HPEERENUM hPeerEnum = NULL;
 
    hr = PeerGraphEnumNodes(hGraph, pwzId, &hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cItem = 1; // want only one matching result

        PEER_NODE_INFO ** ppNodeInfo = NULL;

        hr = PeerGraphGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNodeInfo);

        if (SUCCEEDED(hr))
        {
            if ((cItem > 0) && (NULL != ppNodeInfo))
            {
                if ((*ppNodeInfo)->cAddresses > 0)
                {
                    hr = PeerGraphOpenDirectConnection(hGraph, pwzId,
                            &(*ppNodeInfo)->pAddresses[0], &ullConnection);
                }
                PeerGraphFreeData(ppNodeInfo);
            }
        }
        PeerGraphEndEnumeration(hPeerEnum);
    }
    return ullConnection;
}

```



 

 



