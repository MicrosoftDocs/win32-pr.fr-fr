---
description: Les infrastructures de représentation graphique et de regroupement d’homologues permettent aux applications de se connecter directement à un nœud (graphique) ou à un membre (regroupement), puis d’échanger des données directement avec le nœud. Cette connexion est appelée connexion directe.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Connexions directes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f06fde65cf7597ccbec7f2968dbbf7662b4a6491ae59e6aa66b8baa587dc1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011627"
---
# <a name="direct-connections"></a>Connexions directes

Les infrastructures de représentation graphique et de regroupement d’homologues permettent aux applications de se connecter directement à un nœud (graphique) ou à un membre (regroupement), puis d’échanger des données directement avec le nœud. Cette connexion est appelée **connexion directe**.

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Connexions directes à l’aide de l’infrastructure de représentation graphique des pairs

Avant de pouvoir établir une connexion directe entre deux nœuds d’un graphique, les deux nœuds doivent être inscrits pour l’événement de **\_ \_ \_ \_ connexion directe d’événement de graphique pair à pair** . Pour recevoir des données via une connexion directe, les nœuds doivent également être inscrits pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement Graph pair** .

**Homologue \_ \_ \_ La \_ connexion directe** à un événement de graphique est un événement qui avertit une application qu’une tentative de connexion directe réussit ou échoue. L’état réel de réussite ou d’échec d’un appel à [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) est retourné dans la structure des [**données d' \_ événement du graphique \_ \_ homologue**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .

Pour créer une connexion directe, une application appelle [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), puis passe un handle au graphique, un pointeur vers l’identité de l’autre nœud qui participe à la connexion et un pointeur vers une structure d’adresse IPv6 pour le nœud participant. L’identité du nœud et l’adresse IPv6 qui sont spécifiées dans l’appel à **PeerGraphOpenDirectConnection** doivent être inscrites pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement du graphique homologue** , ou ne peuvent pas recevoir les données envoyées par un homologue appelant. En cas de réussite, **PeerGraphOpenDirectConnection** retourne un ID de connexion 64 bits. Toutefois, l’homologue doit attendre l’événement de **\_ \_ \_ \_ connexion directe d’événement de groupe pair** avant que l’ID de connexion directe puisse être identifié comme valide.

Une fois qu’une connexion est établie et qu’un ID de connexion valide est confirmé, une application peut appeler [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) pour envoyer les données via la connexion spécifiée par l’ID de connexion valide à l’homologue participant, si l’homologue participant est inscrit pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement de graphique pair** . Les données opaques sont disponibles sous la forme d’une structure de [**\_ données d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_data) dans les [**\_ \_ \_ données entrantes des événements homologues**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retournées par l’événement de **\_ \_ \_ \_ données entrantes de l’événement Graph pair** .

Quand une connexion n’est pas nécessaire, une application appelle [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) avec le descripteur de graphique et l’ID de connexion.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Connexions directes à l’aide de l’infrastructure de regroupement d’homologues

Les connexions directes au sein de l’infrastructure de regroupement d’homologues sont gérées de la même façon que l’infrastructure de représentation graphique des homologues.

Avant de pouvoir établir une connexion directe entre deux membres d’un groupe, les deux membres doivent s’inscrire à l’événement de **\_ \_ \_ \_ connexion directe d’événement de groupe pair** . Si un membre du groupe souhaite recevoir des données via une connexion directe, le membre du groupe doit également s’inscrire à l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe homologue** .

**Homologue \_ \_ \_ La \_ connexion directe d’événement de groupe** est un événement qui avertit une application qu’une tentative de connexion directe réussit ou échoue. L’état réel de réussite ou d’échec d’un appel à [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) est retourné dans la structure [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .

Pour créer une connexion directe, une application appelle [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), puis passe un handle au groupe, un pointeur vers l’identité de l’autre membre qui participera à cette connexion et un pointeur vers une structure d’adresse IPv6 pour le membre participant. Le membre dont l’identité et l’adresse IPv6 sont spécifiées dans l’appel à **PeerGroupOpenDirectConnection** doivent être inscrits pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe homologue** , ou le membre ne peut pas recevoir les données envoyées par un homologue appelant. **PeerGroupOpenDirectConnection** retourne un ID de connexion 64 bits en cas de réussite. Toutefois, un homologue doit attendre que l’événement de **\_ \_ \_ \_ connexion directe d’événement de graphique pair** soit déclenché avant que l’ID de connexion directe puisse être identifié comme valide.

Une fois qu’une connexion est établie et qu’un ID de connexion valide est confirmé, une application peut appeler [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) pour envoyer des données via une connexion spécifiée par l’ID de connexion valide à l’homologue participant, si l’homologue participant est inscrit pour l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe pair** . Les données opaques sont disponibles en tant que structure de [**\_ données homologues**](/windows/desktop/api/P2P/ns-p2p-peer_data) dans les [**\_ \_ \_ données entrantes des événements homologues**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) retournées par l’événement de **\_ \_ \_ \_ données entrantes de l’événement de groupe pair** .

Lorsque la connexion n’est pas nécessaire, l’application appelle [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) avec le descripteur de groupe et l’ID de connexion.

## <a name="example-of-a-direct-connection-for-graphing"></a>Exemple de connexion directe pour la représentation graphique


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



 

 



