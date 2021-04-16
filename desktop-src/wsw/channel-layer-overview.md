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
# <a name="channel-layer-overview"></a><span data-ttu-id="43a15-106">Vue d’ensemble de la couche de canal</span><span class="sxs-lookup"><span data-stu-id="43a15-106">Channel Layer Overview</span></span>

<span data-ttu-id="43a15-107">La couche de canal fournit une abstraction du canal de transport ainsi que des messages envoyés sur le canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-107">The Channel Layer provides an abstraction of the transport channel as well as messages sent out on the channel.</span></span> <span data-ttu-id="43a15-108">Il comprend également des fonctions pour la sérialisation des types de données C vers et à partir de structures SOAP.</span><span class="sxs-lookup"><span data-stu-id="43a15-108">It also includes functions for the serialization of C data types to and from SOAP structures.</span></span> <span data-ttu-id="43a15-109">La couche de canal permet un contrôle total des communications au moyen de [messages](message.md) contenant des données envoyées ou reçues, contenant des corps et des en-têtes, ainsi que des [canaux](channel.md) qui extraient les protocoles d’échange de messages et fournissent des propriétés pour personnaliser les paramètres.</span><span class="sxs-lookup"><span data-stu-id="43a15-109">The Channel Layer enables full control of communications by means of [messages](message.md) consisting of data sent or received and containing bodies and headers, and [channels](channel.md) that abstract message exchange protocols and provide properties for customizing settings.</span></span>

## <a name="message"></a><span data-ttu-id="43a15-110">Message</span><span class="sxs-lookup"><span data-stu-id="43a15-110">Message</span></span>

<span data-ttu-id="43a15-111">Un [message](message.md) est un objet qui encapsule des données réseau, en particulier les données transmises ou reçues sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="43a15-111">A [message](message.md) is an object that encapsulates network data — specifically, data that is transmitted or received over a network.</span></span> <span data-ttu-id="43a15-112">La structure du message est définie par SOAP, avec un ensemble discret d’en-têtes et un corps de message.</span><span class="sxs-lookup"><span data-stu-id="43a15-112">The message structure is defined by SOAP, with a discrete set of headers and a message body.</span></span> <span data-ttu-id="43a15-113">Les en-têtes sont placés dans une mémoire tampon et le corps du message est lu ou écrit à l’aide d’une API de flux.</span><span class="sxs-lookup"><span data-stu-id="43a15-113">The headers are placed in a memory buffer, and the message body is read or written using a stream API.</span></span>

![Diagramme montrant l’en-tête et le corps d’un message.](images/messageenvelope.png)

<span data-ttu-id="43a15-115">Bien que le modèle de données d’un message soit toujours le modèle de données XML, le format de câble réel est flexible.</span><span class="sxs-lookup"><span data-stu-id="43a15-115">Although the data model of a message is always the XML data model, the actual wire format is flexible.</span></span> <span data-ttu-id="43a15-116">Avant qu’un message soit transmis, il est encodé à l’aide d’un encodage particulier (tel que texte, binaire ou MTOM).</span><span class="sxs-lookup"><span data-stu-id="43a15-116">Before a message is transmitted, it is encoded using a particular encoding (such as Text, Binary, or MTOM).</span></span> <span data-ttu-id="43a15-117">Pour plus d’informations sur les encodages, consultez l' [**\_ encodage WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .</span><span class="sxs-lookup"><span data-stu-id="43a15-117">See [**WS\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for more information on encodings.</span></span>

![Diagramme montrant plusieurs formats d’encodage de message.](images/messageandencodings.png)

## <a name="channel"></a><span data-ttu-id="43a15-119">Channel</span><span class="sxs-lookup"><span data-stu-id="43a15-119">Channel</span></span>

<span data-ttu-id="43a15-120">Un [canal](channel.md) est un objet utilisé pour envoyer et recevoir des messages sur un réseau entre deux points de terminaison ou plus.</span><span class="sxs-lookup"><span data-stu-id="43a15-120">A [channel](channel.md) is an object used to send and receive messages on a network between two or more endpoints.</span></span>

<span data-ttu-id="43a15-121">Les chaînes ont des données associées qui décrivent comment [adresser](endpoint-address.md) le message lors de son envoi.</span><span class="sxs-lookup"><span data-stu-id="43a15-121">Channels have associated data that describes how to [address](endpoint-address.md) the message when it is sent.</span></span> <span data-ttu-id="43a15-122">L’envoi d’un message sur un canal est semblable au placement d’un message dans un gouffre : le canal inclut les informations relatives à l’emplacement du message et comment l’y accéder.</span><span class="sxs-lookup"><span data-stu-id="43a15-122">Sending a message on a channel is like placing it in a chute — the channel includes the information where the message should go and how to get it there.</span></span>

![Diagramme montrant les canaux pour les messages.](images/channelsaschute.png)

<span data-ttu-id="43a15-124">Les canaux sont classés en [**types de canaux**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="43a15-124">Channels are categorized into [**channel types**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="43a15-125">Un type de canal spécifie la direction vers laquelle les messages peuvent circuler.</span><span class="sxs-lookup"><span data-stu-id="43a15-125">A channel type specifies which direction messages can flow.</span></span> <span data-ttu-id="43a15-126">Le type de canal indique également si le canal est de type session ou sans session.</span><span class="sxs-lookup"><span data-stu-id="43a15-126">The channel type also identifies whether the channel is sessionful, or sessionless.</span></span> <span data-ttu-id="43a15-127">Une session est définie comme un moyen abstrait de mettre en corrélation des messages entre deux parties ou plus.</span><span class="sxs-lookup"><span data-stu-id="43a15-127">A session is defined as an abstract way of correlating messages between two or more parties.</span></span> <span data-ttu-id="43a15-128">Un canal TCP, qui utilise la connexion TCP comme implémentation de session concrète, est un exemple de canal de session.</span><span class="sxs-lookup"><span data-stu-id="43a15-128">An example of a sessionful channel is a TCP channel, which uses the TCP connection as the concrete session implementation.</span></span> <span data-ttu-id="43a15-129">Un exemple de canal sans session est UDP, qui n’a pas de mécanisme de session sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="43a15-129">An example of a sessionless channel is UDP, which does not have an underlying session mechanism.</span></span> <span data-ttu-id="43a15-130">Bien que HTTP possède des connexions TCP sous-jacentes, ce fait n’est pas directement exposé par le biais de cette API et, par conséquent, HTTP est également considéré comme un canal sans session.</span><span class="sxs-lookup"><span data-stu-id="43a15-130">Although HTTP does have underlying TCP connections, this fact is not directly exposed through this API and therefore HTTP is also considered a sessionless channel.</span></span>

![Diagramme montrant les types de canaux de session et sans session.](images/channeltypes.png)

<span data-ttu-id="43a15-132">Bien que les types de canal décrivent les informations de direction et de session d’un canal, ils ne spécifient pas comment le canal est implémenté.</span><span class="sxs-lookup"><span data-stu-id="43a15-132">Although channel types describe the direction and session information for a channel, they do not specify how the channel is implemented.</span></span> <span data-ttu-id="43a15-133">Quel protocole le canal doit-il utiliser ?</span><span class="sxs-lookup"><span data-stu-id="43a15-133">What protocol should the channel use?</span></span> <span data-ttu-id="43a15-134">Comment le canal doit-il tenter de remettre le message ?</span><span class="sxs-lookup"><span data-stu-id="43a15-134">How hard should the channel try to deliver the message?</span></span> <span data-ttu-id="43a15-135">Quel type de sécurité est utilisé ?</span><span class="sxs-lookup"><span data-stu-id="43a15-135">What kind of security is used?</span></span> <span data-ttu-id="43a15-136">S’agit-il d’Singlecast ou de la multidiffusion ?</span><span class="sxs-lookup"><span data-stu-id="43a15-136">Is it singlecast or multicast?</span></span> <span data-ttu-id="43a15-137">Ces paramètres sont appelés « liaison » du canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-137">These settings are referred to as the "binding" of the channel.</span></span> <span data-ttu-id="43a15-138">La liaison se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="43a15-138">The binding consists of the following:</span></span>

-   <span data-ttu-id="43a15-139">Une [**\_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), qui identifie le protocole de transfert à utiliser (TCP, UDP, http, NAMEDPIPE).</span><span class="sxs-lookup"><span data-stu-id="43a15-139">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use (TCP, UDP, HTTP, NAMEDPIPE).</span></span>
-   <span data-ttu-id="43a15-140">Une [**\_ \_ Description de la sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), qui spécifie comment sécuriser le canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-140">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="43a15-141">Définit des [**\_ \_ Propriétés WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), qui spécifient des paramètres facultatifs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="43a15-141">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings.</span></span> <span data-ttu-id="43a15-142">Pour obtenir la liste des propriétés, consultez [**\_ ID de \_ propriété \_ WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .</span><span class="sxs-lookup"><span data-stu-id="43a15-142">See [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) for the list of properties.</span></span>

![Diagramme montrant une liste de propriétés de canal.](images/channelsandbindings.png)

## <a name="listener"></a><span data-ttu-id="43a15-144">Écouteur</span><span class="sxs-lookup"><span data-stu-id="43a15-144">Listener</span></span>

<span data-ttu-id="43a15-145">Pour commencer à communiquer, le client crée un objet de canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-145">To start communicating, the client creates a Channel object.</span></span> <span data-ttu-id="43a15-146">Mais comment le service obtient-il son objet de canal ?</span><span class="sxs-lookup"><span data-stu-id="43a15-146">But how does the service get its Channel object?</span></span> <span data-ttu-id="43a15-147">Pour ce faire, il crée un [écouteur](listener.md).</span><span class="sxs-lookup"><span data-stu-id="43a15-147">It does so by creating a [Listener](listener.md).</span></span> <span data-ttu-id="43a15-148">La création d’un écouteur requiert les mêmes informations de liaison que celles nécessaires pour créer un canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-148">Creating a listener requires the same binding information that is necessary to create a channel.</span></span> <span data-ttu-id="43a15-149">Une fois qu’un écouteur a été créé, l’application peut accepter des canaux de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="43a15-149">Once a Listener has been created, the application can Accept Channels from the Listener.</span></span> <span data-ttu-id="43a15-150">Dans la mesure où l’application peut se trouver derrière les canaux acceptant, les écouteurs gardent généralement une file d’attente de canaux prêts à accepter (jusqu’à un quota).</span><span class="sxs-lookup"><span data-stu-id="43a15-150">Since the application may fall behind in accepting channels, listeners typically keep a queue of channels that are ready to accept (up to some quota).</span></span>

![Diagramme montrant les canaux dans la file d’attente de l’écouteur.](images/channelaccept.png)

## <a name="initiating-communication-client"></a><span data-ttu-id="43a15-152">Initiation de la communication (client)</span><span class="sxs-lookup"><span data-stu-id="43a15-152">Initiating Communication (client)</span></span>

<span data-ttu-id="43a15-153">Pour initier la communication sur le client, utilisez la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="43a15-153">To initiate communication on the client, use the following sequence.</span></span>

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

## <a name="accepting-communication-server"></a><span data-ttu-id="43a15-154">Acceptation de la communication (serveur)</span><span class="sxs-lookup"><span data-stu-id="43a15-154">Accepting Communication (server)</span></span>

<span data-ttu-id="43a15-155">Pour accepter les communications entrantes sur le serveur, utilisez la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="43a15-155">To accept incoming communications on the server, use the following sequence.</span></span>

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

## <a name="sending-messages-client-or-server"></a><span data-ttu-id="43a15-156">Envoi de messages (client ou serveur)</span><span class="sxs-lookup"><span data-stu-id="43a15-156">Sending Messages (client or server)</span></span>

<span data-ttu-id="43a15-157">Pour envoyer des messages, utilisez la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="43a15-157">To send messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="43a15-158">La fonction [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) n’autorise pas la diffusion en continu et suppose que le corps contient un seul élément.</span><span class="sxs-lookup"><span data-stu-id="43a15-158">The [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) function does not allow for streaming, and assumes that the body contains only one element.</span></span> <span data-ttu-id="43a15-159">Pour éviter ces contraintes, utilisez la séquence suivante au lieu de **WsSendMessage**.</span><span class="sxs-lookup"><span data-stu-id="43a15-159">To avoid these constraints, use the following sequence instead of **WsSendMessage**.</span></span>

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

<span data-ttu-id="43a15-160">La fonction [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) utilise la sérialisation pour écrire les éléments body.</span><span class="sxs-lookup"><span data-stu-id="43a15-160">The [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) function uses serialization to write the body elements.</span></span> <span data-ttu-id="43a15-161">Pour écrire les données directement dans le Writer XML, utilisez la séquence suivante au lieu de **WsWriteBody**.</span><span class="sxs-lookup"><span data-stu-id="43a15-161">To write the data directly to the XML Writer, use the following sequence instead of **WsWriteBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

<span data-ttu-id="43a15-162">La fonction [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) utilise la sérialisation pour définir les en-têtes dans la mémoire tampon d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="43a15-162">The [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) function uses serialization to set the headers to the header buffer of the message.</span></span> <span data-ttu-id="43a15-163">Pour utiliser l’enregistreur XML pour écrire un en-tête, utilisez la séquence suivante au lieu de **WsAddCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="43a15-163">To use the XML Writer to write a header, use the following sequence instead of **WsAddCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a><span data-ttu-id="43a15-164">Réception de messages (client ou serveur)</span><span class="sxs-lookup"><span data-stu-id="43a15-164">Receiving Messages (client or server)</span></span>

<span data-ttu-id="43a15-165">Pour recevoir des messages, utilisez la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="43a15-165">To receive messages, use the following sequence.</span></span>

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

<span data-ttu-id="43a15-166">La fonction [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) n’autorise pas la diffusion en continu et suppose que le corps contient un seul élément, et que le type du message (action et schéma du corps) est connu au préalable.</span><span class="sxs-lookup"><span data-stu-id="43a15-166">The [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) function does not allow for streaming, and assumes that the body contains only one element, and that the type of the message (action and schema of the body) is known up front.</span></span> <span data-ttu-id="43a15-167">Pour éviter ces contraintes, utilisez la séquence suivante au lieu de **WsReceiveMessage**.</span><span class="sxs-lookup"><span data-stu-id="43a15-167">To avoid these constraints, use the following sequence instead of **WsReceiveMessage**.</span></span>

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

<span data-ttu-id="43a15-168">La fonction [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) utilise la sérialisation pour lire les éléments body.</span><span class="sxs-lookup"><span data-stu-id="43a15-168">The [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) function uses serialization to read the body elements.</span></span> <span data-ttu-id="43a15-169">Pour lire les données directement à partir du [lecteur XML](xml-reader.md), utilisez la séquence suivante au lieu de **WsReadBody**.</span><span class="sxs-lookup"><span data-stu-id="43a15-169">To read the data directly from the [XML Reader](xml-reader.md), use the following sequence instead of **WsReadBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

<span data-ttu-id="43a15-170">Les fonctions [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) utilisent la sérialisation pour récupérer les en-têtes à partir de la mémoire tampon d’en-tête du message.</span><span class="sxs-lookup"><span data-stu-id="43a15-170">The [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) functions use serialization to get the headers from the header buffer of the message.</span></span> <span data-ttu-id="43a15-171">Pour utiliser le [lecteur XML](xml-reader.md) pour lire un en-tête, utilisez la séquence suivante au lieu de **WsGetCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="43a15-171">To use the [XML Reader](xml-reader.md) to read a header, use the following sequence instead of **WsGetCustomHeader**.</span></span>

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

## <a name="request-reply-client"></a><span data-ttu-id="43a15-172">Demande de réponse (client)</span><span class="sxs-lookup"><span data-stu-id="43a15-172">Request Reply (client)</span></span>

<span data-ttu-id="43a15-173">L’exécution d’une requête-réponse sur le client peut être effectuée à l’aide de la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="43a15-173">Performing a request-reply on the client can be done with the following sequence.</span></span>

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

<span data-ttu-id="43a15-174">La fonction [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) part du principe qu’il existe un seul élément pour le corps des messages de demande et de réponse, et que le type du message (action et schéma du corps) est connu à l’avance.</span><span class="sxs-lookup"><span data-stu-id="43a15-174">The [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) function assumes a single element for the body of the request and reply messages, and that the type of the message (action and schema of the body) are known up front.</span></span> <span data-ttu-id="43a15-175">Pour éviter ces limitations, le message de demande et de réponse peut être envoyé manuellement, comme indiqué dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="43a15-175">To avoid these limitations, the request and reply message can be sent manually, as shown in the following sequence.</span></span> <span data-ttu-id="43a15-176">Cette séquence correspond à la séquence précédente pour l’envoi et la réception d’un message, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="43a15-176">This sequence matches the earlier sequence for sending and receiving a message, except where noted.</span></span>

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

## <a name="request-reply-server"></a><span data-ttu-id="43a15-177">Répondre à la demande (serveur)</span><span class="sxs-lookup"><span data-stu-id="43a15-177">Request Reply (server)</span></span>

<span data-ttu-id="43a15-178">Pour recevoir un message de demande sur le serveur, utilisez la même séquence que celle décrite dans la section précédente sur la réception des messages.</span><span class="sxs-lookup"><span data-stu-id="43a15-178">To receive a request message on the server, use the same sequence as outlined in the previous section on receiving messages.</span></span>

<span data-ttu-id="43a15-179">Pour envoyer un message de réponse ou d’erreur, utilisez la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="43a15-179">To send a reply or fault message, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="43a15-180">La fonction [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) suppose un élément unique dans le corps et n’autorise pas la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="43a15-180">The [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) function assumes a single element in the body and does not allow for streaming.</span></span> <span data-ttu-id="43a15-181">Pour éviter ces limitations, utilisez la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="43a15-181">To avoid these limitations, use the following sequence.</span></span> <span data-ttu-id="43a15-182">Il est identique à la séquence précédente pour l’envoi d’un message, mais utilise le [**\_ \_ message WS reply**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) au lieu du **\_ \_ message WS Blank** lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="43a15-182">This is the same as the earlier sequence for sending a message, but uses [**WS\_REPLY\_MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) instead of **WS\_BLANK\_MESSAGE** when initializing.</span></span>

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

## <a name="message-exchange-patterns"></a><span data-ttu-id="43a15-183">Modèles d’échange de messages</span><span class="sxs-lookup"><span data-stu-id="43a15-183">Message Exchange Patterns</span></span>

<span data-ttu-id="43a15-184">Le [**\_ \_ type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) détermine le modèle d’échange de messages possible pour un canal donné.</span><span class="sxs-lookup"><span data-stu-id="43a15-184">The [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) dictates the message exchange pattern possible for a given channel.</span></span> <span data-ttu-id="43a15-185">Le type pris en charge varie en fonction de la liaison, comme suit :</span><span class="sxs-lookup"><span data-stu-id="43a15-185">The type supported, varies according to the binding, as follows:</span></span>

-   <span data-ttu-id="43a15-186">[**WS \_ La \_ \_ liaison de canal http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge la [**\_ \_ \_ demande de type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et le type de **\_ canal WS \_ \_ répond** sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="43a15-186">[**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_REPLY** on the server.</span></span>
-   <span data-ttu-id="43a15-187">[**WS \_ La \_ \_ liaison de canal TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge la [**\_ \_ \_ \_ session duplex du type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et la **\_ \_ \_ \_ session duplex de type duplex** sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="43a15-187">[**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION** on the server.</span></span>
-   <span data-ttu-id="43a15-188">[**WS \_ La \_ \_ liaison de canal UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge le [**type de \_ canal WS \_ \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et l’entrée de **\_ type de canal \_ \_ WS** sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="43a15-188">[**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>
-   <span data-ttu-id="43a15-189">[**WS \_ La \_ \_ liaison de canal NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge le [**type de \_ canal WS \_ \_ duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) sur le client et l’entrée de **\_ type de canal \_ \_ WS** sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="43a15-189">[**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>

## <a name="message-loops"></a><span data-ttu-id="43a15-190">Boucles de messages</span><span class="sxs-lookup"><span data-stu-id="43a15-190">Message Loops</span></span>

<span data-ttu-id="43a15-191">Pour chaque modèle d’échange de messages, il existe une « boucle » spécifique qui peut être utilisée pour envoyer ou recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="43a15-191">For each message exchange pattern, there is a specific "loop" that can be used to send or receive messages.</span></span> <span data-ttu-id="43a15-192">La boucle décrit l’ordre légal des opérations nécessaires pour envoyer/recevoir plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="43a15-192">The loop describes the legal order of operations necessary to send/receive multiple messages.</span></span> <span data-ttu-id="43a15-193">Les boucles sont décrites ci-dessous en tant que productions grammaticales.</span><span class="sxs-lookup"><span data-stu-id="43a15-193">The loops are describes below as grammar productions.</span></span> <span data-ttu-id="43a15-194">Le terme « final » est une réception dans laquelle les **\_ \_ terminaisons WS S** sont renvoyées (voir les [valeurs de retour des services Web Windows](windows-web-services-return-values.md)), ce qui indique qu’aucun autre message n’est disponible sur le canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-194">The 'end' term is a receive where **WS\_S\_END** is returned (See [Windows Web Services Return Values](windows-web-services-return-values.md)), indicating no more messages are available on the channel.</span></span> <span data-ttu-id="43a15-195">La production parallèle spécifie que, pour Parallel (x & y), l’opération x peut être effectuée simultanément avec y.</span><span class="sxs-lookup"><span data-stu-id="43a15-195">The parallel production specifies that for parallel(x & y) that operation x may be done concurrently with y.</span></span>

<span data-ttu-id="43a15-196">Les boucles suivantes sont utilisées sur le client :</span><span class="sxs-lookup"><span data-stu-id="43a15-196">The following loops are used on the client:</span></span>

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

<span data-ttu-id="43a15-197">Les boucles suivantes sont utilisées sur le serveur :</span><span class="sxs-lookup"><span data-stu-id="43a15-197">The following loops are used on the server:</span></span>

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

<span data-ttu-id="43a15-198">L’utilisation de la [**liaison de sécurité de message de \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sur le serveur nécessite une réception réussie avant que l’envoi soit autorisé, même avec un canal de type [**WS \_ Channel \_ type \_ \_ session duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="43a15-198">Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="43a15-199">Après la première réception.</span><span class="sxs-lookup"><span data-stu-id="43a15-199">After the first receive.</span></span> <span data-ttu-id="43a15-200">la boucle normale s’applique.</span><span class="sxs-lookup"><span data-stu-id="43a15-200">the regular loop applies.</span></span>

<span data-ttu-id="43a15-201">Notez que les canaux de [**type \_ \_ \_ demande de type de canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) et **\_ \_ \_ réponse de type WS** peuvent être utilisés pour envoyer et recevoir des messages unidirectionnels (ainsi que le modèle de demande-réponse standard).</span><span class="sxs-lookup"><span data-stu-id="43a15-201">Note that channels of type [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) and **WS\_CHANNEL\_TYPE\_REPLY** can be used to send and receive one-way messages (as well as the standard request-reply pattern).</span></span> <span data-ttu-id="43a15-202">Pour ce faire, vous devez fermer le canal de réponse sans envoyer de réponse.</span><span class="sxs-lookup"><span data-stu-id="43a15-202">This is accomplished by closing the reply channel without sending a reply.</span></span> <span data-ttu-id="43a15-203">Dans ce cas, aucune réponse n’est reçue sur le canal de demande.</span><span class="sxs-lookup"><span data-stu-id="43a15-203">In this case, there will be no reply received on the request channel.</span></span> <span data-ttu-id="43a15-204">La valeur de retour de **WS \_ S \_** à l’aide de la [**liaison de sécurité de message de \_ contexte de sécurité \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sur le serveur nécessite une réception réussie avant que l’envoi soit autorisé, même avec un canal de type **WS \_ Channel \_ type \_ \_ session duplex**.</span><span class="sxs-lookup"><span data-stu-id="43a15-204">The return value **WS\_S\_END** Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**.</span></span> <span data-ttu-id="43a15-205">Après la première réception, la boucle normale s’applique.</span><span class="sxs-lookup"><span data-stu-id="43a15-205">After the first receive the regular loop applies.</span></span>

<span data-ttu-id="43a15-206">est retourné, ce qui indique qu’aucun message n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="43a15-206">will be returned, indicating no message available.</span></span>

<span data-ttu-id="43a15-207">Les boucles client ou serveur peuvent être effectuées en parallèle les unes avec les autres à l’aide d’instances de canaux multiples.</span><span class="sxs-lookup"><span data-stu-id="43a15-207">Client or server loops may be done in parallel with each other by using multiple channel instances.</span></span>

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a><span data-ttu-id="43a15-208">Filtrage des messages</span><span class="sxs-lookup"><span data-stu-id="43a15-208">Message Filtering</span></span>

<span data-ttu-id="43a15-209">Un canal serveur peut filtrer les messages reçus qui ne sont pas destinés à l’application, tels que les messages qui établissent un [contexte de sécurité](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="43a15-209">A server channel may filter received messages that are not intended for the application, such as messages that establish a [security context](security-context.md).</span></span> <span data-ttu-id="43a15-210">Dans ce cas, la **\_ \_ terminaison de WS S** est retournée à partir de [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) et aucun message d’application n’est disponible sur ce canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-210">In that case **WS\_S\_END** will be returned from [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) and no application messages will be available on that channel.</span></span> <span data-ttu-id="43a15-211">Toutefois, cela ne signale pas que le client est destiné à mettre fin à la communication avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="43a15-211">However, this does not signal that the client intended to end communication with the server.</span></span> <span data-ttu-id="43a15-212">D’autres messages peuvent être disponibles sur un autre canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-212">More messages may be available on another channel.</span></span> <span data-ttu-id="43a15-213">Consultez [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span><span class="sxs-lookup"><span data-stu-id="43a15-213">See [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span></span>

## <a name="cancellation"></a><span data-ttu-id="43a15-214">Annulation</span><span class="sxs-lookup"><span data-stu-id="43a15-214">Cancellation</span></span>

<span data-ttu-id="43a15-215">La fonction [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) est utilisée pour annuler les e/s en attente pour un canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-215">The [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) function is used to cancel pending IO for a channel.</span></span> <span data-ttu-id="43a15-216">Cette API n’attend pas la fin des opérations d’e/s.</span><span class="sxs-lookup"><span data-stu-id="43a15-216">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="43a15-217">Pour plus d’informations, consultez le diagramme d’état de l' [**\_ \_ État du canal WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) et la documentation de **WsAbortChannel** .</span><span class="sxs-lookup"><span data-stu-id="43a15-217">See the [**WS\_CHANNEL\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) state diagram and documentation for **WsAbortChannel** for more information.</span></span>

<span data-ttu-id="43a15-218">L’API [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) est utilisée pour annuler les e/s en attente pour un écouteur.</span><span class="sxs-lookup"><span data-stu-id="43a15-218">The [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API is used to cancel pending IO for a listener.</span></span> <span data-ttu-id="43a15-219">Cette API n’attend pas la fin des opérations d’e/s.</span><span class="sxs-lookup"><span data-stu-id="43a15-219">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="43a15-220">L’abandon d’un écouteur entraîne également l’abandon de toutes les acceptations en attente.</span><span class="sxs-lookup"><span data-stu-id="43a15-220">Aborting a listener will cause any pending accepts to be aborted as well.</span></span> <span data-ttu-id="43a15-221">Pour plus d’informations, consultez le diagramme d’état de l’état de l' [**\_ écouteur \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) et **WsAbortListener** .</span><span class="sxs-lookup"><span data-stu-id="43a15-221">See the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) state diagram and **WsAbortListener** for more information.</span></span>

## <a name="tcp"></a><span data-ttu-id="43a15-222">TCP</span><span class="sxs-lookup"><span data-stu-id="43a15-222">TCP</span></span>

<span data-ttu-id="43a15-223">La [**\_ liaison de \_ canal \_ WS TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur TCP.</span><span class="sxs-lookup"><span data-stu-id="43a15-223">The [**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over TCP.</span></span> <span data-ttu-id="43a15-224">La spécification SOAP sur TCP s’appuie sur le mécanisme de tramage .NET.</span><span class="sxs-lookup"><span data-stu-id="43a15-224">The SOAP over TCP specification builds upon the .NET Framing mechanism.</span></span>

<span data-ttu-id="43a15-225">Le partage de ports n’est pas pris en charge dans cette version.</span><span class="sxs-lookup"><span data-stu-id="43a15-225">Port sharing is not supported in this version.</span></span> <span data-ttu-id="43a15-226">Chaque écouteur ouvert doit utiliser un numéro de port différent.</span><span class="sxs-lookup"><span data-stu-id="43a15-226">Each listener that is opened must use a different port number.</span></span>

## <a name="udp"></a><span data-ttu-id="43a15-227">UDP</span><span class="sxs-lookup"><span data-stu-id="43a15-227">UDP</span></span>

<span data-ttu-id="43a15-228">La [**\_ liaison de \_ canal \_ UDP WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur UDP.</span><span class="sxs-lookup"><span data-stu-id="43a15-228">The [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over UDP.</span></span>

<span data-ttu-id="43a15-229">La liaison UDP présente un certain nombre de limitations :</span><span class="sxs-lookup"><span data-stu-id="43a15-229">There are a number of limitations with the UDP binding:</span></span>

-   <span data-ttu-id="43a15-230">La sécurité n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="43a15-230">There is no support for security.</span></span>
-   <span data-ttu-id="43a15-231">Les messages peuvent être perdus ou dupliqués.</span><span class="sxs-lookup"><span data-stu-id="43a15-231">Messages may be lost or duplicated.</span></span>
-   <span data-ttu-id="43a15-232">Un seul encodage est pris en charge : [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span><span class="sxs-lookup"><span data-stu-id="43a15-232">Only one encoding is supported: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span></span>
-   <span data-ttu-id="43a15-233">Les messages sont fondamentalement limités à 64 Ko et ont souvent une plus grande chance d’être perdus si la taille dépasse la MTU du réseau.</span><span class="sxs-lookup"><span data-stu-id="43a15-233">Messages are fundamentally limited to 64k, and frequently have a greater chance being lost if the size exceeds the MTU of the network.</span></span>

## <a name="http"></a><span data-ttu-id="43a15-234">HTTP</span><span class="sxs-lookup"><span data-stu-id="43a15-234">HTTP</span></span>

<span data-ttu-id="43a15-235">La [**\_ liaison de \_ canal \_ http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur http.</span><span class="sxs-lookup"><span data-stu-id="43a15-235">The [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over HTTP.</span></span>

<span data-ttu-id="43a15-236">Pour contrôler les en-têtes spécifiques à HTTP sur le client et le serveur, consultez [**\_ mappage de \_ message \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span><span class="sxs-lookup"><span data-stu-id="43a15-236">To control HTTP specific headers on the client and server, see [**WS\_HTTP\_MESSAGE\_MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span></span>

<span data-ttu-id="43a15-237">Pour envoyer et recevoir des messages non-SOAP sur le serveur, utilisez [**WS \_ Encoding \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) pour l' [**\_ \_ \_ encodage de propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="43a15-237">To send and receive non-SOAP messages on the server, use [**WS\_ENCODING\_RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

## <a name="namedpipes"></a><span data-ttu-id="43a15-238">NAMEDPIPES</span><span class="sxs-lookup"><span data-stu-id="43a15-238">NAMEDPIPES</span></span>

<span data-ttu-id="43a15-239">La [**\_ liaison de \_ canal \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) prend en charge SOAP sur les canaux nommés, ce qui permet la communication avec le service Windows Communication Foundation (WCF) à l’aide de NetNamedPipeBinding.</span><span class="sxs-lookup"><span data-stu-id="43a15-239">The [**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over named pipes, allowing communication with the Windows Communication Foundation (WCF) service using NetNamedPipeBinding.</span></span>

## <a name="correlating-requestreply-messages"></a><span data-ttu-id="43a15-240">Corrélation des messages de demande/réponse</span><span class="sxs-lookup"><span data-stu-id="43a15-240">Correlating Request/Reply Messages</span></span>

<span data-ttu-id="43a15-241">Les messages de demande/réponse sont corrélés de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="43a15-241">Request/Reply messages are correlated in one of two ways:</span></span>

-   <span data-ttu-id="43a15-242">La corrélation est effectuée en utilisant le canal comme mécanisme de corrélation.</span><span class="sxs-lookup"><span data-stu-id="43a15-242">Correlation is done using the channel as the correlation mechanism.</span></span> <span data-ttu-id="43a15-243">Par exemple, lors de l’utilisation du [**\_ transport de \_ version \_ WS d’adressage**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) et de la [**liaison de \_ \_ canal \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , la réponse pour le message de demande est corrélée à la demande par le fait qu’il s’agit du corps d’entité de la réponse http.</span><span class="sxs-lookup"><span data-stu-id="43a15-243">For example, when using [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) the reply for the request message is correlated to the request by the fact that is it is the entity body of the HTTP response.</span></span>
-   <span data-ttu-id="43a15-244">La corrélation s’effectue à l’aide des en-têtes MessageID et latesto.</span><span class="sxs-lookup"><span data-stu-id="43a15-244">Correlation is done using the MessageID and RelatesTo headers.</span></span> <span data-ttu-id="43a15-245">Ce mécanisme est utilisé avec [**WS \_ adressage \_ version \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) et **WS \_ adressage \_ version \_ 0 \_ 9** (même en cas d’utilisation de la [**\_ \_ \_ liaison de canal http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span><span class="sxs-lookup"><span data-stu-id="43a15-245">This mechanism is used with [**WS\_ADDRESSING\_VERSION\_1\_0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and **WS\_ADDRESSING\_VERSION\_0\_9** (even when using [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span></span> <span data-ttu-id="43a15-246">Dans ce cas, le message de demande comprend l’en-tête MessageID.</span><span class="sxs-lookup"><span data-stu-id="43a15-246">In this case, the request message includes the MessageID header.</span></span> <span data-ttu-id="43a15-247">Le message de réponse inclut un en-tête rerécento qui a la valeur de l’en-tête MessageID de la demande.</span><span class="sxs-lookup"><span data-stu-id="43a15-247">The response message includes a RelatesTo header that has the value of the request's MessageID header.</span></span> <span data-ttu-id="43a15-248">L’en-tête replus récent permet au client de mettre en corrélation une réponse avec une demande qu’il a envoyée.</span><span class="sxs-lookup"><span data-stu-id="43a15-248">The RelatesTo header allows the client to correlate a response with a request it sent.</span></span>

<span data-ttu-id="43a15-249">Les API de couche de canal suivantes utilisent automatiquement les mécanismes de corrélation appropriés basés sur la [**\_ \_ version d’adressage WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) du canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-249">The following channel layer APIs automatically use the appropriate correlation mechanisms based on the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) of the channel.</span></span>

-   [<span data-ttu-id="43a15-250">**WsRequestReply**</span><span class="sxs-lookup"><span data-stu-id="43a15-250">**WsRequestReply**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [<span data-ttu-id="43a15-251">**WsSendReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="43a15-251">**WsSendReplyMessage**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [<span data-ttu-id="43a15-252">**WsSendFaultMessageForError**</span><span class="sxs-lookup"><span data-stu-id="43a15-252">**WsSendFaultMessageForError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

<span data-ttu-id="43a15-253">Si ces API ne sont pas utilisées, les en-têtes peuvent être ajoutés manuellement et accessibles à l’aide de [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) ou [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span><span class="sxs-lookup"><span data-stu-id="43a15-253">If these APIs are not used, the headers can be manually added and accessed using [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) or [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span></span>

## <a name="custom-channels-and-listeners"></a><span data-ttu-id="43a15-254">Canaux et écouteurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="43a15-254">Custom Channels and Listeners</span></span>

<span data-ttu-id="43a15-255">Si l’ensemble prédéfini de liaisons de canal ne répond pas aux besoins de l’application, une implémentation de canal et d’écouteur personnalisé peut être définie en spécifiant [**la \_ \_ \_ liaison de canal personnalisé WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) lors de la création du canal ou de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="43a15-255">If the predefined set of channel bindings do not meet the needs of the application, then a custom channel and listener implementation can be defined by specifying [**WS\_CUSTOM\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) when creating the channel or listener.</span></span> <span data-ttu-id="43a15-256">L’implémentation réelle du canal/écouteur est spécifiée sous la forme d’un ensemble de rappels via des rappels de [**\_ \_ \_ canal personnalisé de \_ \_ propriété WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ou des propriétés de rappel de l' [**\_ \_ \_ \_ écouteur \_ personnalisé**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) de la propriété de l’écouteur WS.</span><span class="sxs-lookup"><span data-stu-id="43a15-256">The actual implementation of the channel/listener is specified as a set of callbacks via [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) or [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties.</span></span> <span data-ttu-id="43a15-257">Une fois qu’un canal ou écouteur personnalisé a été créé, le résultat est un objet [WS \_ Channel](ws-channel.md) ou [WS \_ Listener](ws-listener.md) qui peut être utilisé avec les API existantes.</span><span class="sxs-lookup"><span data-stu-id="43a15-257">Once a custom channel or listener are created, the result is a [WS\_CHANNEL](ws-channel.md) or [WS\_LISTENER](ws-listener.md) object that can be used with existing APIs.</span></span>

<span data-ttu-id="43a15-258">Un canal et un écouteur personnalisés peuvent également être utilisés avec le proxy de service et l' [hôte de service](service-host.md) en spécifiant la valeur de **\_ \_ \_ liaison de canal personnalisé WS** dans l’énumération de [**\_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) et les [**\_ \_ \_ \_ \_ rappels de canal personnalisé**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) de la propriété WS Channel et les propriétés de [**\_ \_ \_ \_ \_ rappels de l’écouteur personnalisé**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) de la propriété de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="43a15-258">A custom channel and listener can also be used with Service Proxy and [Service Host](service-host.md) by specifying the **WS\_CUSTOM\_CHANNEL\_BINDING** value in the [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) enumeration and the [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) and [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties when creating the Service Proxy or Service Host.</span></span>

## <a name="security"></a><span data-ttu-id="43a15-259">Sécurité</span><span class="sxs-lookup"><span data-stu-id="43a15-259">Security</span></span>

<span data-ttu-id="43a15-260">Le canal permet de limiter la quantité de mémoire utilisée pour divers aspects des opérations via des propriétés telles que :</span><span class="sxs-lookup"><span data-stu-id="43a15-260">The channel allows limiting the amount of memory used for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="43a15-261">[**WS \_ \_ \_ taille maximale des \_ \_ messages \_ mis en mémoire tampon**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-261">[**WS\_CHANNEL\_PROPERTY\_MAX\_BUFFERED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-262">[**WS \_ \_ \_ taille maximale des \_ \_ messages \_ diffusés en continu**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-262">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-263">[**WS \_ \_ \_ \_ \_ \_ taille maximale de début**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-263">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_START\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-264">[**WS \_ \_ \_ taille maximale des \_ \_ \_ en- \_ \_ têtes de demande http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-264">[**WS\_CHANNEL\_PROPERTY\_MAX\_HTTP\_REQUEST\_HEADERS\_BUFFER\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-265">[**WS \_ \_ \_ taille maximale du \_ \_ dictionnaire de \_ sessions**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-265">[**WS\_CHANNEL\_PROPERTY\_MAX\_SESSION\_DICTIONARY\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="43a15-266">Ces propriétés ont des valeurs par défaut qui sont restrictives et sécurisées pour la plupart des scénarios.</span><span class="sxs-lookup"><span data-stu-id="43a15-266">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="43a15-267">Les valeurs par défaut et toutes les modifications qui y sont apportées doivent être évaluées avec soin par rapport aux vecteurs d’attaque potentiels qui peuvent provoquer un déni de service par un utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="43a15-267">Default values and any modifications to them should be carefully evaluated against potential attack vectors which may cause denial of service by a remote user.</span></span>

<span data-ttu-id="43a15-268">Le canal permet de définir des valeurs de délai d’attente pour différents aspects des opérations via des propriétés telles que :</span><span class="sxs-lookup"><span data-stu-id="43a15-268">The channel allows setting timeout values for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="43a15-269">[**WS \_ \_délai de \_ connexion \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-269">[**WS\_CHANNEL\_PROPERTY\_CONNECT\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-270">[**WS \_ \_ \_ \_ délai d’envoi**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-270">[**WS\_CHANNEL\_PROPERTY\_SEND\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-271">[**WS \_ \_délai de \_ \_ réponse de \_ réception**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-271">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_RESPONSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-272">[**WS \_ \_délai de \_ réception \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-272">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-273">[**WS \_ \_délai de \_ résolution \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal,</span><span class="sxs-lookup"><span data-stu-id="43a15-273">[**WS\_CHANNEL\_PROPERTY\_RESOLVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="43a15-274">[**WS \_ \_délai de \_ fermeture \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)de la propriété de canal.</span><span class="sxs-lookup"><span data-stu-id="43a15-274">[**WS\_CHANNEL\_PROPERTY\_CLOSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="43a15-275">Ces propriétés ont des valeurs par défaut qui sont restrictives et sécurisées pour la plupart des scénarios.</span><span class="sxs-lookup"><span data-stu-id="43a15-275">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="43a15-276">L’augmentation des valeurs de délai d’attente augmente la durée pendant laquelle une partie distante peut conserver une ressource locale active, telle que la mémoire, les sockets et les threads qui exécutent des e/s synchrones.</span><span class="sxs-lookup"><span data-stu-id="43a15-276">Increasing timeout values increases the amount of time that a remote party can hold a local resource alive, such as memory, sockets, and threads doing synchronous I/O.</span></span> <span data-ttu-id="43a15-277">Une application doit évaluer les valeurs par défaut et être prudente lors de l’extension d’un délai d’attente, car elle peut ouvrir des vecteurs d’attaque potentiels qui peuvent provoquer un déni de service à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="43a15-277">An application should evaluate the default values and use caution when increasing a timeout as it may open up potential attack vectors which may cause denial of service from a remote computer.</span></span>

<span data-ttu-id="43a15-278">Certaines des autres options de configuration et considérations relatives à la conception des applications qui doivent être évaluées avec soin lors de l’utilisation de l’API de canal WWSAPI :</span><span class="sxs-lookup"><span data-stu-id="43a15-278">Some of the other configuration options and application design considerations that should be carefully evaluated when using WWSAPI Channel API:</span></span>

-   <span data-ttu-id="43a15-279">Lors de l’utilisation de la couche canal/écouteur, il revient à l’application de créer et d’accepter des canaux côté serveur.</span><span class="sxs-lookup"><span data-stu-id="43a15-279">When using the channel/listener layer, it is up to the application to create and accept channels on the server side.</span></span> <span data-ttu-id="43a15-280">De même, il revient à l’application de créer et d’ouvrir des canaux côté client.</span><span class="sxs-lookup"><span data-stu-id="43a15-280">Similarly, it is up to the application to create and open channels on the client side.</span></span> <span data-ttu-id="43a15-281">Une application doit placer une limite supérieure sur ces opérations, car chaque canal consomme de la mémoire et d’autres ressources limitées, telles que les sockets.</span><span class="sxs-lookup"><span data-stu-id="43a15-281">An application should put an upper bound on these operations because each channel consumes memory and other limited resources such as sockets.</span></span> <span data-ttu-id="43a15-282">Une application doit être particulièrement prudente lorsque vous créez un canal en réponse à une action déclenchée par un tiers distant.</span><span class="sxs-lookup"><span data-stu-id="43a15-282">An application should be especially careful when create a channel in response to any action triggered by a remote party.</span></span>
-   <span data-ttu-id="43a15-283">C’est à l’application d’écrire la logique pour créer des canaux et les accepter.</span><span class="sxs-lookup"><span data-stu-id="43a15-283">It is up to the application to write the logic to create channels and accept them.</span></span> <span data-ttu-id="43a15-284">Chaque canal consomme des ressources limitées, telles que la mémoire et les sockets.</span><span class="sxs-lookup"><span data-stu-id="43a15-284">Each channel consumes limited resources such as memory and sockets.</span></span> <span data-ttu-id="43a15-285">Une application doit avoir une limite supérieure pour le nombre de canaux qu’elle est disposé à accepter, ou une partie distante peut établir de nombreuses connexions, conduisant à insuffisance et donc à un déni de service.</span><span class="sxs-lookup"><span data-stu-id="43a15-285">An application should have an upper bound on the number of channels it is willing to accept, or a remote party could make many connections, leading to OOM and hence denial of service.</span></span> <span data-ttu-id="43a15-286">Il doit également recevoir activement les messages de ces connexions à l’aide d’un petit délai d’expiration.</span><span class="sxs-lookup"><span data-stu-id="43a15-286">It should also actively receive messages from those connections using a small timeout.</span></span> <span data-ttu-id="43a15-287">Si aucun message n’est reçu, l’opération expire et la connexion doit être libérée.</span><span class="sxs-lookup"><span data-stu-id="43a15-287">If no messages are received, then the operation will time out and the connection should be released.</span></span>
-   <span data-ttu-id="43a15-288">Il revient à une application d’envoyer une réponse ou une erreur en interprétant les en-têtes SOAP ReplyTo ou FaultTo.</span><span class="sxs-lookup"><span data-stu-id="43a15-288">It is up to an application to send a reply or fault by interpreting the ReplyTo or FaultTo SOAP headers.</span></span> <span data-ttu-id="43a15-289">La pratique sécurisée consiste à honorer uniquement un en-tête ReplyTo ou FaultTo qui est « Anonymous », ce qui signifie que la connexion existante (TCP, HTTP) ou l’adresse IP source (UDP) doit être utilisée pour envoyer la réponse SOAP.</span><span class="sxs-lookup"><span data-stu-id="43a15-289">The secure practice is to only honor a ReplyTo or FaultTo header which is "anonymous", meaning that the existing connection (TCP, HTTP) or source IP (UDP) should be used to send the SOAP reply.</span></span> <span data-ttu-id="43a15-290">Les applications doivent faire preuve de prudence lors de la création de ressources (par exemple, un canal) afin de répondre à une autre adresse, sauf si le message a été signé par un tiers qui peut parler de l’adresse à laquelle la réponse est envoyée.</span><span class="sxs-lookup"><span data-stu-id="43a15-290">Applications should exercise extreme caution when creating resources (such as a channel) in order to reply to a different address, unless the message was signed by a party that can speak for the address that the reply is being sent to.</span></span>
-   <span data-ttu-id="43a15-291">La validation effectuée dans la couche de canal n’est pas un remplacement de l’intégrité des données obtenue par la sécurité.</span><span class="sxs-lookup"><span data-stu-id="43a15-291">The validation done in the channel layer is no replacement for data integrity achieved through security.</span></span> <span data-ttu-id="43a15-292">Une application doit s’appuyer sur les fonctionnalités de sécurité de WWSAPI pour s’assurer qu’elle communique avec une entité approuvée et doit également s’appuyer sur la sécurité pour garantir l’intégrité des données.</span><span class="sxs-lookup"><span data-stu-id="43a15-292">An application must rely on security features of the WWSAPI to ensure that it is communicating with a trusted entity, and must also rely on security to ensure data integrity.</span></span>

<span data-ttu-id="43a15-293">De même, il existe des options de configuration des messages et des considérations relatives à la conception des applications qui doivent être évaluées avec soin lors de l’utilisation de l’API de message WWSAPI :</span><span class="sxs-lookup"><span data-stu-id="43a15-293">Similarly, there are message configuration options and application design considerations that should be carefully evaluated when using WWSAPI Message API:</span></span>

-   <span data-ttu-id="43a15-294">La taille du tas utilisé pour stocker les en-têtes d’un message peut être configurée à l’aide de la propriété [**Propriétés du segment de \_ propriété du message \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="43a15-294">The size of the heap used to store the headers of a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_HEAP\_PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="43a15-295">L’amélioration de cette valeur permet d’utiliser davantage de mémoire par les en-têtes du message, ce qui peut entraîner des insuffisance.</span><span class="sxs-lookup"><span data-stu-id="43a15-295">Increasing this value allows more memory to be consumed by the headers of the message, which can lead to OOM.</span></span>
-   <span data-ttu-id="43a15-296">L’utilisateur de l’objet de message doit se rendre compte que les API d’accès en-tête sont O (n) en ce qui concerne le nombre d’en-têtes dans le message, car ils vérifient les doublons.</span><span class="sxs-lookup"><span data-stu-id="43a15-296">The user of the message object must realize that the header access APIs are O(n) with respect to the number of headers in the message, since they check for duplicates.</span></span> <span data-ttu-id="43a15-297">Les conceptions qui requièrent de nombreux en-têtes dans un message peuvent entraîner une utilisation excessive du processeur.</span><span class="sxs-lookup"><span data-stu-id="43a15-297">Designs which require many headers in a message may lead to excessive CPU usage.</span></span>
-   <span data-ttu-id="43a15-298">Le nombre maximal d’en-têtes dans un message peut être configuré à l’aide de la propriété [**WS \_ message \_ Property \_ Max \_ processed \_ headers**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="43a15-298">The maximum number of headers in a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_MAX\_PROCESSED\_HEADERS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="43a15-299">Il existe également une limite implicite en fonction de la taille du segment de mémoire du message.</span><span class="sxs-lookup"><span data-stu-id="43a15-299">There is also an implicit limit based on the size of the heap of the message.</span></span> <span data-ttu-id="43a15-300">L’amélioration de ces deux valeurs permet d’afficher davantage d’en-têtes, ce qui complique le temps nécessaire pour trouver un en-tête (lors de l’utilisation des API d’accès en-tête).</span><span class="sxs-lookup"><span data-stu-id="43a15-300">Increasing both of these values allows more headers to be present, which compounds the time necessary to find a header (when using the header access APIs).</span></span>

 

 




