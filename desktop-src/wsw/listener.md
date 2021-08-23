---
title: Écouteur
description: Un écouteur est utilisé par le client pour accepter un canal entrant d’un service.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Services Web de l’écouteur pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26a2f9951dedefd5fb686de7935a76ce3b6ef24dcea140d5414b713e89ad1f1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026377"
---
# <a name="listener"></a>Écouteur

Un écouteur est utilisé par le client pour accepter un [canal](channel.md) entrant d’un service.

Pour créer un écouteur du, vous spécifiez le type de canal en tant que valeur d’énumération de [**\_ \_ type WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , les informations de [liaison](binding.md) et l' [URL](url.md) à écouter.


Pour commencer à écouter sur l’URL, appelez la fonction [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .

Pour accepter les communications entrantes, appelez [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).

Pour annuler les e/s en attente pour un écouteur, appelez [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Pour plus d’informations sur les transitions d’État pour un écouteur, consultez l’énumération de l’état de l' [**\_ \_ écouteur WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .

Les rappels suivants font partie de l’écouteur :

-   [**rappel de l' \_ \_ écouteur WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_rappel de \_ canal d’acceptation WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**rappel de l' \_ \_ écouteur WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ créer un \_ canal \_ pour le rappel de l' \_ écouteur \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**création d’un \_ \_ rappel d’ÉCOUTEur WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**rappel de l' \_ \_ écouteur gratuit WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**rappel de la propriété de l' \_ \_ ÉCOUTEur WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**rappel de l' \_ \_ écouteur WS Open \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**rappel de l' \_ écouteur de réinitialisation WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**rappel de la propriété de l' \_ \_ écouteur WS Set \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Les énumérations suivantes font partie de l’écouteur :

-   [**\_version WS IP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**ID de propriété de l' \_ écouteur WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**État de l' \_ écouteur WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Les fonctions suivantes font partie de l’écouteur :

-   [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**WsCloseListener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**WsFreeListener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**WsGetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**WsResetListener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**WsSetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

Le handle suivant fait partie de l’écouteur :

-   [\_écouteur WS](ws-listener.md)

Les structures suivantes font partie de l’écouteur :

-   [**\_ \_ rappels de l’écouteur personnalisé WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**\_ \_ sous- \_ chaînes de l’agent utilisateur non autorisées WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**\_noms d’hôte WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**Propriétés de l' \_ écouteur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**propriété de l' \_ écouteur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




