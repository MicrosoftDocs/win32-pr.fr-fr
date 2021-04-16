---
title: Vue d’ensemble de la couche de canal
description: La couche de canal fournit une abstraction du canal de transport ainsi que des messages envoyés sur le canal.
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- Vue d’ensemble des couches de canal services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104557546"
---
# <a name="channel-layer-overview"></a>Vue d’ensemble de la couche de canal

La couche de canal fournit une abstraction du canal de transport ainsi que des messages envoyés sur le canal. Il comprend également des fonctions pour la sérialisation des types de données C vers et à partir de structures SOAP. La couche de canal permet un contrôle total des communications au moyen de [messages](message.md) contenant des données envoyées ou reçues, contenant des corps et des en-têtes, ainsi que des [canaux](channel.md) qui extraient les protocoles d’échange de messages et fournissent des propriétés pour personnaliser les paramètres.

## <a name="message"></a>Message

Un [message](message.md) est un objet qui encapsule des données réseau, en particulier les données transmises ou reçues sur un réseau. La structure du message est définie par SOAP, avec un ensemble discret d’en-têtes et un corps de message. Les en-têtes sont placés dans une mémoire tampon et le corps du message est lu ou écrit à l’aide d’une API de flux.

![Diagramme montrant l’en-tête et le corps d’un message.](images/messageenvelope.png)

Bien que le modèle de données d’un message soit toujours le modèle de données XML, le format de câble réel est flexible. Avant qu’un message soit transmis, il est encodé à l’aide d’un encodage particulier (tel que texte, binaire ou MTOM). Pour plus d’informations sur les encodages, consultez l' [**\_ encodage WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .

![Diagramme montrant plusieurs formats d’encodage de message.](images/messageandencodings.png)

## <a name="channel"></a>Channel

Un [canal](channel.md) est un objet utilisé pour envoyer et recevoir des messages sur un réseau entre deux points de terminaison ou plus.

Les chaînes ont des données associées qui décrivent comment [adresser](endpoint-address.md) le message lors de son envoi. L’envoi d’un message sur un canal est semblable au placement d’un message dans un gouffre : le canal inclut les informations relatives à l’emplacement du message et comment l’y accéder.

![Diagramme montrant les canaux pour les messages.](images/channelsaschute.png)

Les canaux sont classés en [**types de canaux**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Un type de canal spécifie la direction vers laquelle les messages peuvent circuler. Le type de canal indique également si le canal est de type session ou sans session. Une session est définie comme un moyen abstrait de mettre en corrélation des messages entre deux parties ou plus. Un canal TCP, qui utilise la connexion TCP comme implémentation de session concrète, est un exemple de canal de session. Un exemple de canal sans session est UDP, qui n’a pas de mécanisme de session sous-jacent. Bien que HTTP possède des connexions TCP sous-jacentes, ce fait n’est pas directement exposé par le biais de cette API et, par conséquent, HTTP est également considéré comme un canal sans session.

![Diagramme montrant les types de canaux de session et sans session.](images/channeltypes.png)

Bien que les types de canal décrivent les informations de direction et de session d’un canal, ils ne spécifient pas comment le canal est implémenté. Quel protocole le canal doit-il utiliser ? Comment le canal doit-il tenter de remettre le message ? Quel type de sécurité est utilisé ? S’agit-il d’Singlecast ou de la multidiffusion ? Ces paramètres sont appelés « liaison » du canal. La liaison se compose des éléments suivants :

-   Une [**\_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), qui identifie le protocole de transfert à utiliser (TCP, UDP, http, NAMEDPIPE).
-   Une [**\_ \_ Description de la sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), qui spécifie comment sécuriser le canal.
-   Définit des [**\_ \_ Propriétés WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), qui spécifient des paramètres facultatifs supplémentaires. Pour obtenir la liste des propriétés, consultez [**\_ ID de \_ propriété \_ WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .

![Diagramme montrant une liste de propriétés de canal.](images/channelsandbindings.png)

## <a name="listener"></a>Écouteur

Pour commencer à communiquer, le client crée un objet de canal. Mais comment le service obtient-il son objet de canal ? Pour ce faire, il crée un [écouteur](listener.md). La création d’un écouteur requiert les mêmes informations de liaison que celles nécessaires pour créer un canal. Une fois qu’un écouteur a été créé, l’application peut accepter des canaux de l’écouteur. Dans la mesure où l’application peut se trouver derrière les canaux acceptant, les écouteurs gardent généralement une file d’attente de canaux prêts à accepter (jusqu’à un quota).

![Diagramme montrant les canaux dans la file d’attente de l’écouteur.](images/channelaccept.png)

## <a name="initiating-communication-client"></a>Initiation de la communication (client)

Pour initier la communication sur le client, utilisez la séquence suivante.

``` syntax
WsCreateChannel
for each address being sent to
{
    WsOpenChannel           // open channel to address
    // send and/or receive messages
    WsCloseChannel          // close channel
    WsResetChannel?         // reset if opening again
}
WsFreeChannel
```

## <a name="accepting-communication-server"></a>Acceptation de la communication (serveur)

Pour accepter les communications entrantes sur le serveur, utilisez la séquence suivante.

``` syntax
WsCreateListener
WsOpenListener
for each channel being accepted (can be done in parallel)
{
    WsCreateChannelForListener
    for each accept
    {
        WsAcceptChannel     // accept the channel
        // send and/or receive messages
        WsCloseChannel      // close the channel
        WsResetChannel?     // reset if accepting again
    }
    WsFreeChannel
}
WsCloseListener
WsFreeListener
```

## <a name="sending-messages-client-or-server"></a>Envoi de messages (client ou serveur)

Pour envoyer des messages, utilisez la séquence suivante.

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La fonction [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) n’autorise pas la diffusion en continu et suppose que le corps contient un seul élément. Pour éviter ces contraintes, utilisez la séquence suivante au lieu de **WsSendMessage**.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

La fonction [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) utilise la sérialisation pour écrire les éléments body. Pour écrire les données directement dans le Writer XML, utilisez la séquence suivante au lieu de **WsWriteBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

La fonction [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) utilise la sérialisation pour définir les en-têtes dans la mémoire tampon d’en-tête du message. Pour utiliser l’enregistreur XML pour écrire un en-tête, utilisez la séquence suivante au lieu de **WsAddCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a>Réception de messages (client ou serveur)

Pour recevoir des messages, utilisez la séquence suivante.

``` syntax
WsCreateMessageForChannel
for each message being received
{
    WsReceiveMessage            // receive a message
    WsGetHeader*                // optionally access standard headers such as To or Action
    WsResetMessage              // reset if reading another message
}
WsFreeMessage
```

La fonction [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) n’autorise pas la diffusion en continu et suppose que le corps contient un seul élément, et que le type du message (action et schéma du corps) est connu au préalable. Pour éviter ces contraintes, utilisez la séquence suivante au lieu de **WsReceiveMessage**.

``` syntax
WsReadMessageStart              // read all headers into header buffer
for each standard header
{
    WsGetHeader                 // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader           // deserialize application defined header
}
for each element of the body
{
    WsFillBody?                 // optionally fill the body
    WsReadBody                  // deserialize element of body
}
WsReadMessageEnd                // read end of message
```

La fonction [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) utilise la sérialisation pour lire les éléments body. Pour lire les données directement à partir du [lecteur XML](xml-reader.md), utilisez la séquence suivante au lieu de **WsReadBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

Les fonctions [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) utilisent la sérialisation pour récupérer les en-têtes à partir de la mémoire tampon d’en-tête du message. Pour utiliser le [lecteur XML](xml-reader.md) pour lire un en-tête, utilisez la séquence suivante au lieu de **WsGetCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateReader                      // create an xml reader
WsSetInputToBuffer                  // specify input of reader should be buffer
WsMoveReader*                       // move to inside header element
while looking for header to read
{
    WsReadToStartElement            // see if the header matches the application header
    if header matched
    {
        WsGetHeaderAttributes?      // get the standard header attributes
        WsReadStartElement          // consume the start of the header element
        // use the read functions to read the contents of the header element
        WsReadEndElement            // consume the end of the header element
    }
    else
    {
        WsSkipNode                  // skip the header element
    }
}                
```

## <a name="request-reply-client"></a>Demande de réponse (client)

L’exécution d’une requête-réponse sur le client peut être effectuée à l’aide de la séquence suivante.

``` syntax
WsCreateMessageForChannel               // create request message 
WsCreateMessageForChannel               // create reply message 
for each request reply
{
    WsRequestReply                      // send request, receive reply
    WsResetMessage?                     // reset request message (if repeating)
    WsResetMessage?                     // reset reply message (if repeating)
}
WsFreeMessage                           // free request message
WsFreeMessage                           // free reply message
```

La fonction [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) part du principe qu’il existe un seul élément pour le corps des messages de demande et de réponse, et que le type du message (action et schéma du corps) est connu à l’avance. Pour éviter ces limitations, le message de demande et de réponse peut être envoyé manuellement, comme indiqué dans l’ordre suivant. Cette séquence correspond à la séquence précédente pour l’envoi et la réception d’un message, sauf indication contraire.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message

// the following block is specific to sending a request
{
    generate a unique MessageID for request
    WsSetHeader         // set the message ID            
}

for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message

WsReadMessageStart      // read all headers into header buffer

// the following is specific to receiving a reply
{
    WsGetHeader         // deserialize RelatesTo ID of reply
    verify request MessageID is equal to RelatesTo ID
}

for each standard header
{
    WsGetHeader         // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader   // deserialize application defined header
}
for each element of the body
{
    WsFillBody?         // optionally fill the body
    WsReadBody          // deserialize element of body
}
WsReadMessageEnd        // read end of message                
```

## <a name="request-reply-server"></a>Répondre à la demande (serveur)

Pour recevoir un message de demande sur le serveur, utilisez la même séquence que celle décrite dans la section précédente sur la réception des messages.

Pour envoyer un message de réponse ou d’erreur, utilisez la séquence suivante.

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

La fonction [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) suppose un élément unique dans le corps et n’autorise pas la diffusion en continu. Pour éviter ces limitations, utilisez la séquence suivante. Il est identique à la séquence précédente pour l’envoi d’un message, mais utilise le [**\_ \_ message WS reply**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) au lieu du **\_ \_ message WS Blank** lors de l’initialisation.

``` syntax
// the following block is specific to sending a reply
{
    WsInitializeMessage // initialize message to WS_REPLY_MESSAGE
}
WsSetHeader             // serialize action header into header buffer                                
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

## <a name="message-exchange-patterns"></a>Modèles d’échange de messages

Le [**\_ \_ type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) détermine le modèle d’échange de messages possible pour un canal donné. Le type pris en charge varie en fonction de la liaison, comme suit :

-   [**WS \_ La \_ \_ liaison de canal http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge la [**\_ \_ \_ demande de type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et le type de **\_ canal WS \_ \_ répond** sur le serveur.
-   [**WS \_ La \_ \_ liaison de canal TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge la [**\_ \_ \_ \_ session duplex du type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et la **\_ \_ \_ \_ session duplex de type duplex** sur le serveur.
-   [**WS \_ La \_ \_ liaison de canal UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge le [**type de \_ canal WS \_ \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et l’entrée de **\_ type de canal \_ \_ WS** sur le serveur.
-   [**WS \_ La \_ \_ liaison de canal NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge le [**type de \_ canal WS \_ \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et l’entrée de **\_ type de canal \_ \_ WS** sur le serveur.

## <a name="message-loops"></a>Boucles de messages

Pour chaque modèle d’échange de messages, il existe une « boucle » spécifique qui peut être utilisée pour envoyer ou recevoir des messages. La boucle décrit l’ordre légal des opérations nécessaires pour envoyer/recevoir plusieurs messages. Les boucles sont décrites ci-dessous en tant que productions grammaticales. Le terme « final » est une réception dans laquelle les **\_ \_ terminaisons WS S** sont renvoyées (voir les [valeurs de retour des services Web Windows](windows-web-services-return-values.md)), ce qui indique qu’aucun autre message n’est disponible sur le canal. La production parallèle spécifie que, pour Parallel (x & y), l’opération x peut être effectuée simultanément avec y.

Les boucles suivantes sont utilisées sur le client :

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

Les boucles suivantes sont utilisées sur le serveur :

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

L’utilisation de la [**liaison de sécurité de message de \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sur le serveur nécessite une réception réussie avant que l’envoi soit autorisé, même avec un canal de type [**WS \_ Channel \_ type \_ \_ session duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Après la première réception. la boucle normale s’applique.

Notez que les canaux de [**type \_ \_ \_ demande de type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) et **\_ \_ \_ réponse de type WS** peuvent être utilisés pour envoyer et recevoir des messages unidirectionnels (ainsi que le modèle de demande-réponse standard). Pour ce faire, vous devez fermer le canal de réponse sans envoyer de réponse. Dans ce cas, aucune réponse n’est reçue sur le canal de demande. La valeur de retour de **WS \_ S \_** à l’aide de la [**liaison de sécurité de message de \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sur le serveur nécessite une réception réussie avant que l’envoi soit autorisé, même avec un canal de type **WS \_ Channel \_ type \_ \_ session duplex**. Après la première réception, la boucle normale s’applique.

est retourné, ce qui indique qu’aucun message n’est disponible.

Les boucles client ou serveur peuvent être effectuées en parallèle les unes avec les autres à l’aide d’instances de canaux multiples.

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>Filtrage des messages

Un canal serveur peut filtrer les messages reçus qui ne sont pas destinés à l’application, tels que les messages qui établissent un [contexte de sécurité](security-context.md). Dans ce cas, la **\_ \_ terminaison de WS S** est retournée à partir de [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) et aucun message d’application n’est disponible sur ce canal. Toutefois, cela ne signale pas que le client est destiné à mettre fin à la communication avec le serveur. D’autres messages peuvent être disponibles sur un autre canal. Consultez [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).

## <a name="cancellation"></a>Annulation

La fonction [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) est utilisée pour annuler les e/s en attente pour un canal. Cette API n’attend pas la fin des opérations d’e/s. Pour plus d’informations, consultez le diagramme d’état de l' [**\_ \_ État du canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) et la documentation de **WsAbortChannel** .

L’API [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) est utilisée pour annuler les e/s en attente pour un écouteur. Cette API n’attend pas la fin des opérations d’e/s. L’abandon d’un écouteur entraîne également l’abandon de toutes les acceptations en attente. Pour plus d’informations, consultez le diagramme d’état de l’état de l' [**\_ écouteur \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) et **WsAbortListener** .

## <a name="tcp"></a>TCP

La [**\_ liaison de \_ canal \_ WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur TCP. La spécification SOAP sur TCP s’appuie sur le mécanisme de tramage .NET.

Le partage de ports n’est pas pris en charge dans cette version. Chaque écouteur ouvert doit utiliser un numéro de port différent.

## <a name="udp"></a>UDP

La [**\_ liaison de \_ canal \_ UDP WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur UDP.

La liaison UDP présente un certain nombre de limitations :

-   La sécurité n’est pas prise en charge.
-   Les messages peuvent être perdus ou dupliqués.
-   Un seul encodage est pris en charge : [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).
-   Les messages sont fondamentalement limités à 64 Ko et ont souvent une plus grande chance d’être perdus si la taille dépasse la MTU du réseau.

## <a name="http"></a>HTTP

La [**\_ liaison de \_ canal \_ http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur http.

Pour contrôler les en-têtes spécifiques à HTTP sur le client et le serveur, consultez [**\_ mappage de \_ message \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).

Pour envoyer et recevoir des messages non-SOAP sur le serveur, utilisez [**WS \_ Encoding \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) pour l' [**\_ \_ \_ encodage de propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

## <a name="namedpipes"></a>NAMEDPIPES

La [**\_ liaison de \_ canal \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur les canaux nommés, ce qui permet la communication avec le service Windows Communication Foundation (WCF) à l’aide de NetNamedPipeBinding.

## <a name="correlating-requestreply-messages"></a>Corrélation des messages de demande/réponse

Les messages de demande/réponse sont corrélés de l’une des deux manières suivantes :

-   La corrélation est effectuée en utilisant le canal comme mécanisme de corrélation. Par exemple, lors de l’utilisation du [**\_ transport de \_ version \_ WS d’adressage**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) et de la [**liaison de \_ \_ canal \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , la réponse pour le message de demande est corrélée à la demande par le fait qu’il s’agit du corps d’entité de la réponse http.
-   La corrélation s’effectue à l’aide des en-têtes MessageID et latesto. Ce mécanisme est utilisé avec [**WS \_ adressage \_ version \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) et **WS \_ adressage \_ version \_ 0 \_ 9** (même en cas d’utilisation de la [**\_ \_ \_ liaison de canal http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)). Dans ce cas, le message de demande comprend l’en-tête MessageID. Le message de réponse inclut un en-tête rerécento qui a la valeur de l’en-tête MessageID de la demande. L’en-tête replus récent permet au client de mettre en corrélation une réponse avec une demande qu’il a envoyée.

Les API de couche de canal suivantes utilisent automatiquement les mécanismes de corrélation appropriés basés sur la [**\_ \_ version d’adressage WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) du canal.

-   [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

Si ces API ne sont pas utilisées, les en-têtes peuvent être ajoutés manuellement et accessibles à l’aide de [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) ou [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).

## <a name="custom-channels-and-listeners"></a>Canaux et écouteurs personnalisés

Si l’ensemble prédéfini de liaisons de canal ne répond pas aux besoins de l’application, une implémentation de canal et d’écouteur personnalisé peut être définie en spécifiant [**la \_ \_ \_ liaison de canal personnalisé WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) lors de la création du canal ou de l’écouteur. L’implémentation réelle du canal/écouteur est spécifiée sous la forme d’un ensemble de rappels via des rappels de [**\_ \_ \_ canal personnalisé de \_ \_ propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ou des propriétés de rappel de l' [**\_ \_ \_ \_ écouteur \_ personnalisé**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) de la propriété de l’écouteur WS. Une fois qu’un canal ou écouteur personnalisé a été créé, le résultat est un objet [WS \_ Channel](ws-channel.md) ou [WS \_ Listener](ws-listener.md) qui peut être utilisé avec les API existantes.

Un canal et un écouteur personnalisés peuvent également être utilisés avec le proxy de service et l' [hôte de service](service-host.md) en spécifiant la valeur de **\_ \_ \_ liaison de canal personnalisé WS** dans l’énumération de [**\_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) et les [**\_ \_ \_ \_ \_ rappels de canal personnalisé**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) de la propriété WS Channel et les propriétés de [**\_ \_ \_ \_ \_ rappels de l’écouteur personnalisé**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) de la propriété de l’écouteur.

## <a name="security"></a>Sécurité

Le canal permet de limiter la quantité de mémoire utilisée pour divers aspects des opérations via des propriétés telles que :

-   [**WS \_ \_ \_ taille maximale des \_ \_ messages \_ mis en mémoire tampon**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_ \_ taille maximale des \_ \_ messages \_ diffusés en continu**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_ \_ \_ \_ \_ taille maximale de début**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_ \_ taille maximale des \_ \_ \_ en- \_ \_ têtes de demande http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_ \_ taille maximale du \_ \_ dictionnaire de \_ sessions**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal.

Ces propriétés ont des valeurs par défaut qui sont restrictives et sécurisées pour la plupart des scénarios. Les valeurs par défaut et toutes les modifications qui y sont apportées doivent être évaluées avec soin par rapport aux vecteurs d’attaque potentiels qui peuvent provoquer un déni de service par un utilisateur distant.

Le canal permet de définir des valeurs de délai d’attente pour différents aspects des opérations via des propriétés telles que :

-   [**WS \_ \_délai de \_ connexion \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_ \_ \_ délai d’envoi**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_délai de \_ \_ réponse de \_ réception**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_délai de \_ réception \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_délai de \_ résolution \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,
-   [**WS \_ \_délai de \_ fermeture \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal.

Ces propriétés ont des valeurs par défaut qui sont restrictives et sécurisées pour la plupart des scénarios. L’augmentation des valeurs de délai d’attente augmente la durée pendant laquelle une partie distante peut conserver une ressource locale active, telle que la mémoire, les sockets et les threads qui exécutent des e/s synchrones. Une application doit évaluer les valeurs par défaut et être prudente lors de l’extension d’un délai d’attente, car elle peut ouvrir des vecteurs d’attaque potentiels qui peuvent provoquer un déni de service à partir d’un ordinateur distant.

Certaines des autres options de configuration et considérations relatives à la conception des applications qui doivent être évaluées avec soin lors de l’utilisation de l’API de canal WWSAPI :

-   Lors de l’utilisation de la couche canal/écouteur, il revient à l’application de créer et d’accepter des canaux côté serveur. De même, il revient à l’application de créer et d’ouvrir des canaux côté client. Une application doit placer une limite supérieure sur ces opérations, car chaque canal consomme de la mémoire et d’autres ressources limitées, telles que les sockets. Une application doit être particulièrement prudente lorsque vous créez un canal en réponse à une action déclenchée par un tiers distant.
-   C’est à l’application d’écrire la logique pour créer des canaux et les accepter. Chaque canal consomme des ressources limitées, telles que la mémoire et les sockets. Une application doit avoir une limite supérieure pour le nombre de canaux qu’elle est disposé à accepter, ou une partie distante peut établir de nombreuses connexions, conduisant à insuffisance et donc à un déni de service. Il doit également recevoir activement les messages de ces connexions à l’aide d’un petit délai d’expiration. Si aucun message n’est reçu, l’opération expire et la connexion doit être libérée.
-   Il revient à une application d’envoyer une réponse ou une erreur en interprétant les en-têtes SOAP ReplyTo ou FaultTo. La pratique sécurisée consiste à honorer uniquement un en-tête ReplyTo ou FaultTo qui est « Anonymous », ce qui signifie que la connexion existante (TCP, HTTP) ou l’adresse IP source (UDP) doit être utilisée pour envoyer la réponse SOAP. Les applications doivent faire preuve de prudence lors de la création de ressources (par exemple, un canal) afin de répondre à une autre adresse, sauf si le message a été signé par un tiers qui peut parler de l’adresse à laquelle la réponse est envoyée.
-   La validation effectuée dans la couche de canal n’est pas un remplacement de l’intégrité des données obtenue par la sécurité. Une application doit s’appuyer sur les fonctionnalités de sécurité de WWSAPI pour s’assurer qu’elle communique avec une entité approuvée et doit également s’appuyer sur la sécurité pour garantir l’intégrité des données.

De même, il existe des options de configuration des messages et des considérations relatives à la conception des applications qui doivent être évaluées avec soin lors de l’utilisation de l’API de message WWSAPI :

-   La taille du tas utilisé pour stocker les en-têtes d’un message peut être configurée à l’aide de la propriété [**Propriétés du segment de \_ propriété du message \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . L’amélioration de cette valeur permet d’utiliser davantage de mémoire par les en-têtes du message, ce qui peut entraîner des insuffisance.
-   L’utilisateur de l’objet de message doit se rendre compte que les API d’accès en-tête sont O (n) en ce qui concerne le nombre d’en-têtes dans le message, car ils vérifient les doublons. Les conceptions qui requièrent de nombreux en-têtes dans un message peuvent entraîner une utilisation excessive du processeur.
-   Le nombre maximal d’en-têtes dans un message peut être configuré à l’aide de la propriété [**WS \_ message \_ Property \_ Max \_ processed \_ headers**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Il existe également une limite implicite en fonction de la taille du segment de mémoire du message. L’amélioration de ces deux valeurs permet d’afficher davantage d’en-têtes, ce qui complique le temps nécessaire pour trouver un en-tête (lors de l’utilisation des API d’accès en-tête).

 

 




