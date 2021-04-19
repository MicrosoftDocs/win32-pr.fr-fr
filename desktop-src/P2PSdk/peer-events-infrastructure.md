---
description: L’infrastructure homologue utilise des événements pour informer les applications des modifications qui se sont produites au sein d’un réseau pair à pair, par exemple un nœud ajouté ou supprimé dans un graphique.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Infrastructure des événements homologues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6347ad6a7dd0cf2fae4a0aa623bfda48ab0aa9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531951"
---
# <a name="peer-events-infrastructure"></a>Infrastructure des événements homologues

L’infrastructure homologue utilise des événements pour informer les applications des modifications qui se sont produites au sein d’un réseau pair à pair, par exemple un nœud ajouté ou supprimé dans un graphique. Les infrastructures de représentation graphique et de regroupement d’homologues utilisent l’infrastructure des événements homologues.

## <a name="receiving-peer-event-notification"></a>Réception d’une notification d’événement homologue

Un homologue peut s’inscrire pour recevoir une notification lorsqu’un attribut d’un graphique ou d’un groupe est modifié ou qu’un événement homologue spécifique se produit. Une application homologue appelle la fonction [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) ou [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) et passe un handle d’événement à l’infrastructure homologue, créée précédemment par un appel à [**CreateEvent**](graphing-reference-links.md). L’infrastructure homologue utilise le descripteur pour signaler à une application qu’un événement homologue s’est produit.

L’application passe également une série d' [**\_ \_ \_ inscriptions d’événements de graphiques homologues**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) ou de structures d' [**inscription d' \_ événements de groupe \_ \_ homologue**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) qui indiquent à l’infrastructure homologue les événements homologues spécifiques pour lesquels l’application demande une notification. L’application doit également spécifier exactement le nombre de structures passées.

## <a name="peer-graphing-events"></a>Événements de représentation graphique d’homologue

Une application de représentation graphique des homologues peut s’inscrire pour recevoir une notification pour 9 événements de graphique homologue. Chaque nom d’événement est précédé d’un **\_ \_ \_ événement de graphique homologue**, par exemple, l’état du graphique de l' **homologue \_ \_ \_ a changé**. Sauf indication contraire, les informations relatives à une modification sont récupérées à l’aide de [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata).

-   **Homologue \_ L' \_ État de l’événement Graph \_ \_ Changed** indique que l’état d’un graphique a été modifié, par exemple, un nœud a été synchronisé avec un graphique.
-   **Homologue \_ La \_ propriété de l’événement Graph \_ \_ Changed** indique qu’une propriété d’un graphique ou d’un groupe a été modifiée, par exemple, le nom convivial d’un graphique a changé.
    > [!Note]  
    > L’application doit appeler [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) pour obtenir les informations modifiées.

     

-   **Homologue \_ Enregistrement d’événement de graphique \_ \_ \_ modifié** indique qu’un enregistrement a été modifié, par exemple, un enregistrement est supprimé.
-   **Homologue \_ La \_ \_ \_ connexion directe d’événement de graphique** indique qu’une connexion directe a été modifiée, par exemple, un nœud est connecté.
-   **Homologue \_ La \_ \_ \_ connexion du voisin de l’événement Graph** indique qu’une connexion à un nœud voisin a été modifiée, par exemple, un nœud est connecté.
-   **Homologue \_ Les \_ \_ \_ données entrantes de l’événement Graph** indiquent que des données ont été reçues d’une connexion directe ou voisine.
-   **Homologue \_ L' \_ événement Graph \_ Connection \_ Required** indique que l’infrastructure de création de graphiques requiert une nouvelle connexion.
    > [!Note]  
    > Un appel à [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) se connecte à un nouveau nœud. Un appel à [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) ne retourne pas de données.

     

-   **Homologue \_ Le \_ nœud d’événement Graph \_ \_ Changed** indique que les informations de présence du nœud ont été modifiées, par exemple, une adresse IP a changé.
-   **Homologue \_ L' \_ événement \_ de graphique synchronisé** indique qu’un type d’enregistrement spécifique est synchronisé.

Une fois qu’une application a reçu une notification indiquant qu’un événement homologue s’est produit, l’application appelle [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)et passe le handle d’événement homologue retourné par [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent). L’infrastructure homologue retourne un pointeur vers une structure de [**\_ données d' \_ événement \_ de graphique homologue**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) qui contient les données demandées. Cette fonction doit être appelée jusqu’à ce qu' **\_ \_ aucune \_ \_ donnée d’événement** ne soit retournée.

Une fois qu’une application n’a pas besoin d’une notification d’événement homologue, l’application appelle [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)et passe le handle d’événement homologue retourné par [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) lorsque l’application est inscrite.

## <a name="handling-graph-connection-referrals"></a>Gestion des références de connexion au graphique

Quand [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) est appelé, l’homologue qui se connecte est averti de la réussite ou de l’échec par le biais de l’événement de **\_ \_ \_ \_ connexion voisine de l’événement de graphique homologue** asynchrone. Si la connexion a échoué en raison de problèmes de mise en réseau spécifiques (par exemple, un pare-feu mal configuré), l’événement de **\_ \_ \_ \_ connexion voisine de l’événement du graphique homologue** est déclenché, avec l’état de la connexion défini sur **connexion d’égal \_ \_ échec**.

Toutefois, lorsqu’un homologue reçoit une référence lorsqu’il tente de se connecter à un nœud occupé, la **\_ \_ \_ \_ connexion voisine de l’événement du graphique homologue** est déclenchée sur l’homologue qui se connecte, l’état de la connexion ayant la valeur **\_ \_ échec** de la connexion. L’homologue qui se connecte peut être référencé par un autre nœud qui est occupé et peut envoyer une référence, et le même événement et le même État sont déclenchés sur l’homologue qui se connecte. Cette chaîne de références entraînant l’échec de la **\_ connexion \_ homologue** les États des événements peuvent se poursuivre jusqu’à épuisement du nombre maximal de tentatives de connexion. L’homologue n’a pas de mécanisme permettant de déterminer la différence entre une tentative de connexion complète et la référence de connexion.

Pour résoudre ce problème, les développeurs doivent envisager d’utiliser les événements de changement d’État du graphique des homologues pour déterminer si la tentative de connexion a réussi. Si l’événement n’est pas reçu dans un intervalle de temps spécifique, l’application peut supposer que l’homologue qui se connecte est référencé et que l’application homologue doit considérer la tentative de connexion comme une défaillance.

## <a name="peer-grouping-events"></a>Événements de regroupement d’homologues

Une application de regroupement pair peut s’inscrire pour recevoir une notification pour 8 événements homologues. Chaque nom d’événement est précédé d’un **\_ \_ événement \_ de groupe homologue**, par exemple, l’état de l' **événement du groupe homologue \_ \_ \_ \_ a été modifié**. Sauf indication contraire, les informations relatives à une modification sont récupérées à l’aide de [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata).

-   **Homologue \_ État de l’événement de groupe \_ \_ \_ modifié** indique que l’état du groupe a changé. Il existe deux valeurs d’État possibles : l' **État du groupe homologue est à l' \_ \_ \_ écoute**, ce qui indique que le groupe n’a pas de connexion et qu’il attend de nouveaux membres et que l' **État du groupe homologue \_ a des \_ \_ connexions**, ce qui indique que le groupe a au moins une connexion. Cette valeur d’État peut être obtenue en appelant [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) après le déclenchement de cet événement.
-   **Homologue \_ La \_ propriété d’événement de groupe \_ \_ Changed** indique que les propriétés de groupe ont été modifiées ou mises à jour par le créateur du groupe.
-   **Homologue \_ Enregistrement d’événement de groupe \_ \_ \_ modifié** indique qu’une opération d’enregistrement a été effectuée. Cet événement est déclenché lorsqu’un homologue participant au groupe publie, met à jour ou supprime un enregistrement. Par exemple, cet événement est déclenché lorsqu’une application chat envoie un message de conversation.
-   **Homologue \_ Le \_ membre d’événement de groupe \_ \_ Changed** indique que l’état d’un membre dans le groupe a changé. Les changements d’État sont les suivants :
    -   **Homologue \_ MEMBRE \_ connecté**. Un homologue s’est connecté au groupe.
    -   **Homologue \_ MEMBRE \_ déconnecté**. Un homologue s’est déconnecté du groupe.
    -   **Homologue \_ MEMBRE \_ joint**. De nouvelles informations d’appartenance ont été publiées pour un homologue.
    -   **Homologue \_ MEMBRE \_ mis à jour**. Un homologue a été mis à jour avec de nouvelles informations, telles qu’une nouvelle adresse IP.
-   **Homologue \_ \_connexion du \_ voisin \_ d’événement de groupe**. Les pairs qui feront partie des connexions des voisins au sein du groupe doivent s’inscrire à cet événement. Notez que l’inscription à cet événement ne permet pas à l’homologue de recevoir des données ; l’inscription de cet événement garantit uniquement la notification lors de la réception d’une demande de connexion voisine.
-   **Homologue \_ \_ \_ \_ connexion directe d’événement de groupe**. Les pairs qui feront partie des connexions directes au sein du groupe doivent s’inscrire à cet événement. Notez que l’inscription à cet événement ne permet pas à l’homologue de recevoir des données ; l’inscription de cet événement garantit uniquement la notification lors de la réception d’une demande de connexion directe.
-   **Homologue \_ Regroupez les \_ \_ \_ données entrantes**. Les pairs qui recevront des données via un voisin ou une connexion directe doivent s’inscrire à cet événement. Lorsque cet événement est déclenché, les données opaques transmises par l’autre homologue participant peuvent être obtenues en appelant [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Notez que pour recevoir cet événement, l’homologue doit avoir déjà été inscrit pour la connexion **directe d’événement de groupe homologue \_ \_ \_ \_** ou la **\_ \_ \_ \_ connexion voisine d’événement de groupe pair**.
-   **Homologue \_ \_ \_ \_ échec** de la connexion de l’événement de groupe. Une connexion a échoué pour une raison quelconque. Aucune donnée n’est fournie lorsque cet événement est déclenché, et [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) ne doit pas être appelé.

Une fois qu’une application a reçu une notification indiquant qu’un événement homologue s’est produit (à l’exclusion de [](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)l’échec de la **\_ connexion d’événement de groupe \_ \_ \_ pair**), l’application appelle PeerGroupGetEventData et passe le handle d’événement homologue retourné par [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). L’infrastructure homologue retourne un pointeur vers une structure de [**\_ données d' \_ événement \_ de groupe pair**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) qui contient les données demandées. Cette fonction doit être appelée jusqu’à ce qu' **\_ \_ aucune \_ \_ donnée d’événement ne** soit retournée. Quand une application ne requiert plus de notification pour un événement homologue, un appel à [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent)doit être effectué en passant le handle d’événement homologue retourné par **PeerGroupRegisterEvent** lorsque l’application est inscrite pour l’événement particulier.

## <a name="example-of-registering-for-peer-graphing-events"></a>Exemple d’inscription pour les événements de représentation graphique d’homologue

L’exemple de code suivant montre comment s’inscrire auprès des événements de représentation graphique des homologues.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it can be called for only
//           the events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents()
{
    HPEEREVENT  g_hPeerEvent = NULL;        // The one PeerEvent handle
    HANDLE      g_hEvent = NULL;            // Handle signaled by Graphing when we have an event
    HRESULT hr = S_OK;
    PEER_GRAPH_EVENT_REGISTRATION regs[] = {
        { PEER_GRAPH_EVENT_RECORD_CHANGED, 0 },
        { PEER_GRAPH_EVENT_NODE_CHANGED,   0 },
        { PEER_GRAPH_EVENT_STATUS_CHANGED, 0 },
        { PEER_GRAPH_EVENT_DIRECT_CONNECTION, 0 },
        { PEER_GRAPH_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        wprintf(L"CreateEvent call failed.\n");
        hr = E_OUTOFMEMORY;
    }
    else
    {
        hr = PeerGraphRegisterEvent(g_hGraph, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
        if (FAILED(hr))
        {
           wprintf(L"PeerGraphRegisterEvent call failed.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            wprintf(L"Could not set up event callback.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    return hr;
}
```



 

 



